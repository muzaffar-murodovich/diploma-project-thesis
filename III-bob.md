# III BOB. XORAZM SHEVASIDAN ADABIY TILGA TARJIMON DASTURINI LOYIHALASH VA YARATISH

## 3.1. Lug'at ma'lumotlarini to'plash, tozalash va tuzilishi

### 3.1.1. Lug'at tuzilmasini loyihalash

Tarjimon dasturining asosini lug'at ma'lumotlar bazasi tashkil etadi. Ushbu bazaning to'g'ri loyihalanishi butun tizimning ishlash sifatiga bevosita ta'sir qiladi. Loyihalash bosqichida quyidagi asosiy savollarga javob topish zarur bo'ldi: lug'at qanday formatda saqlanadi; har bir yozuv qanday ma'lumotlarni o'z ichiga oladi; ko'p so'zli iboralar qanday boshqariladi; va normalizatsiya qanday amalga oshiriladi.

Lug'at uchun CSV (Comma-Separated Values) formati tanlandi. Bu tanlovning bir necha asosiy sababi bor. Birinchidan, CSV formatida saqlangan ma'lumotlar Python dasturlash tilining standart `csv` kutubxonasi yordamida tez va samarali yuklanadi. Ikkinchidan, CSV fayllarini oddiy matn muharrirlari yoki elektron jadval dasturlari orqali ko'rish va tahrirlash mumkin, bu esa lug'atni doimiy to'ldirish va tuzatish jarayonini osonlashtiradi. Uchinchidan, bu format kichik loyihalarda relyatsion ma'lumotlar bazasining murakkabligini joriy etmasdan, lug'at hajmiga mos samaradorlikni ta'minlaydi.

Lug'atning asosiy tuzilmasi ikki ustundan iborat:

- **`Title`** — Xorazm shevasi so'zi yoki iborasi (kalit)
- **`Meaning`** — adabiy o'zbek tilidagi muqobil yoki izoh (qiymat)

Ushbu ikki ustunli sodda tuzilma tizimning ishlash tezligini oshiradi. Dastur yuklanganda barcha lug'at yozuvlari Python lug'ati (dictionary) ko'rinishida xotiraga yuklanadi: sheva so'zi kalit, adabiy muqobili esa qiymat bo'ladi. Keyin tarjima so'ralganda xotiradan qidirish amalga oshiriladi, bu esa ma'lumotlar bazasiga har safar murojaat qilishga nisbatan ancha tezroq ishlaydi.

### 3.1.2. Manba materiallardan ma'lumot ajratib olish

Lug'at uchun ma'lumotlar uch asosiy manbadan to'plandi. Asosiy manba sifatida "Xorazm shevalari lug'ati" (Norbayeva, Sa'dullayeva, Atabayeva, 2024) tanlangan. Ushbu lug'atning bosma sahifalaridan matn ajratib olish uchun Google Colab muhitida Nvidia T4 GPU da ishga tushirilgan **LightOnOCR-2-1B** modeli qo'llanildi. Bu model Hugging Face platformasida joylashgan bo'lib, diakritik belgilar va noodatiy transkripsiya ramzlarini tanishda standart OCR vositalariga nisbatan ancha yuqori aniqlik ko'rsatdi.

OCR ishlov berish jarayonida xotira yetarlilik muammolariga duch kelindi. Bu muammo sahifalarni kichikroq masshtab parametrida qayta ishlash va har bir sahifadan so'ng CUDA xotirasini tozalash (`torch.cuda.empty_cache()`) orqali hal qilindi. Natijada lug'atning barcha sahifalari matn sifatida ajratib olindi va `ocr_natija.txt` faylida saqlandi.

Ikkinchi manba — Excel formatidagi jadval. Bu jadval oldingi yillardagi dialektologik tadqiqotlar asosida to'plangan bo'lib, taxminan 1340 ta yozuvni o'z ichiga oladi va lotin yozuvida tuzilgan.

Uchinchi manba sifatida S. Ernazarov tomonidan yaratilgan "Xorazmcha" mobil ilovasining (xorazmcha.uz) lug'at ma'lumotlari jalb qilindi. Bu manba kirill yozuvida bo'lganligi sababli, undan foydalanishdan avval lotin yozuviga o'tkazish va normalizatsiya qilish zarur bo'ldi.

### 3.1.3. Ma'lumotlarni tozalash jarayoni

Xom OCR natijalaridan foydalanish mumkin bo'lgan lug'at yozuvlarini olish uchun bir necha bosqichli tozalash jarayoni o'tkazildi. Ushbu jarayon Python tilida yozilgan maxsus `csv_clean.py` skripti orqali amalga oshirildi.

**Normalizatsiya.** `translator.py` dagi `_normalize()`  funksiyasi so'zni qidiruvga tayyorlaydi: harflarni kichik harfga o'tkazadi va tutuq belgisi (`ʻ`, `'`) variantlarini olib tashlaydi. Shu tariqa foydalanuvchi `qoʻl` deb yozsa ham, `qol` deb yozsa ham bir xil yozuv topiladi. Bu normalizatsiya ham lug'at yuklash, ham tarjima so'rovini qayta ishlash bosqichida bir xil qo'llaniladi. Manbalardagi diakritik belgilarni (`ä`, `ö`, `ü` kabi) sodda o'zbek lotin harflariga aylantirish esa alohida tayyorlash bosqichida amalga oshirilgan.

**Dublikatlarni o'chirish.** Birlashtirish jarayonida turli manbalardan bir xil sheva so'zi bir necha marta kirib qolishi mumkin. `csv_clean.py` skripti barcha yozuvlarni alifbo tartibida saralab, dublikatlarni aniqlaydi va kamroq ma'lumotli nusxani o'chiradi. Manba ustunligi tamoyiliga ko'ra "Xorazm shevalari lug'ati" (2024) dagi talqin har doim ustun hisoblanadi.

**Registrni standartlashtirish.** Barcha adabiy muqobil ma'nolar kichik harfda saqlanadi. Tarjima jarayonida esa `_match_case()` funksiyasi kiritilgan so'zning registrini (bosh harf yoki kichik harf) tanib, natijani xuddi shu tartibda formatlaydi. Bu funksiya uchun qoidalar oddiy: agar kiritilgan so'z to'liq bosh harfda bo'lsa, muqobil ham bosh harfda; agar faqat birinchi harfi bosh bo'lsa, muqobilning ham birinchi harfi bosh bo'ladi.

### 3.1.4. Manbalarni birlashtirish

Uchta manbadan olingan CSV fayllarini birlashtirish uchun `merge_dicts.py` skripti ishlab chiqildi. Bu skript quyidagi mantiqqa asoslanadi:

1. Asosiy manba (`output.csv` — OCR orqali olingan "Xorazm shevalari lug'ati" ma'lumotlari) yuklanadi.
2. Qo'shimcha manba (`fromexcel.csv`) yuklanadi va har bir yozuv uchun tekshiriladi: agar asosiy manbada mavjud bo'lsa, o'tkazib yuboriladi; bo'lmasa, qo'shiladi.
3. Natija `output_clean.csv` faylida saqlanadi.

Ushbu yondashuv ilmiy jihatdan eng ishonchli manbaning ustunligini kafolatlaydi. Yakuniy lug'at taxminan **3486 ta yozuvni** o'z ichiga oladi. Bu hajm mavjud o'xshash yechimlar bilan solishtirganda sezilarli darajada katta: masalan, IlhomJabborov tomonidan GitHub'da joylashtirilgan "Translate-Uzbek-Khorazm" loyihasida atigi 100 dan ortiq yozuv mavjud.

---

## 3.2. Foydalanuvchi interfeysi (UI/UX) dizayni va veb-ilova ekranlarini yaratish

### 3.2.1. Interfeys tuzilmasini loyihalash

Tarjimon dasturining foydalanuvchi interfeysi loyihalashda asosiy maqsad — soddalik va samaradorlik o'rtasidagi muvozanatni ta'minlash bo'ldi. Maqsadli foydalanuvchi — Xorazm shevasi so'zlarini adabiy o'zbek tiliga tarjima qilmoqchi bo'lgan har qanday shaxs: talabalar, tilshunoslar, sheva bilan qiziquvchi keng jamoatchilik. Bu foydalanuvchilar doirasi juda keng bo'lganligi sababli, interfeys texnik bilim talab qilmasdan darhol ishlatish mumkin bo'lishi kerak edi.

Interfeys uchun veb-brauzer platformasi tanlandi. Buning bir necha sababi bor: birinchidan, veb-interfeys alohida ilova o'rnatishni talab qilmaydi; ikkinchidan, u istalgan qurilmada — kompyuter, telefon, planshet — ishlaydi; uchinchidan, yangilanishlar foydalanuvchiga avtomatik yetib boradi, chunki hamma narsa serverda joylashgan.

Asosiy ekran uch qismdan iborat: sarlavha paneli, tarjima oynasi va pastki ma'lumot qatori. Tarjima oynasining o'zi esa ikkiga bo'linadi — chap tomonda sheva matni kiritish maydoni, o'ng tomonda adabiy tildagi tarjima natijasi ko'rsatiladi. Ushbu ikki panelli yondashuv Google Translate, DeepL va boshqa zamonaviy tarjimon tizimlarida keng qo'llaniladigan tanish shablon bo'lib, foydalanuvchilar uchun intuitiv hisoblanadi.

### 3.2.2. Vizual dizayn va CSS

Interfeys dizayni CSS o'zgaruvchilari (CSS custom properties) orqali qurilgan bo'lib, rang sxemasi va shrift tizimi yagona joyda boshqariladi. Bu yondashuv kelajakda qorang'i rejim (dark mode) yoki boshqa ranglar sxemasini qo'shishni osonlashtiradi.

Asosiy rang palitrasi: asosiy fon uchun ochiq kulrang (`--bg`), panel foni uchun oq (`--surface`), matn uchun to'q (`--text`), ko'k-binafsha asosiy rang (`--primary`) belgilangan. Ushbu ranglar tanlashda zamonaviy minimal dizayn tamoyillariga rioya qilindi — ortiqcha bezak va ranglar ko'zni charchatmasdan, foydalanuvchini asosiy vazifaga — tarjimaga — yo'naltiradi.

Sarlavha panelida dastur nomi — "Xorazm shevasi tarjimoni" — va lug'at hajmini ko'rsatuvchi badge joylashgan. Badge (`dict-badge`) lug'atda nechta so'z mavjudligini real vaqtda ko'rsatadi: ilovaning har yuklanishida Flask template motori bu qiymatni avtomatik hisoblaydi va sahifaga kiritadi. Bu foydalanuvchiga lug'atning qanchalik katta ekanligini darhol bildirib turadi.

### 3.2.3. Interaktivlik va JavaScript

Tarjima jarayoni sahifani yangilamasdan (real vaqtda) amalga oshiriladi. Buning uchun JavaScript orqali asinxron so'rovlar (Fetch API) ishlatiladi. Foydalanuvchi chap maydonga matn yozishi bilan 300 millisekund kechikishdan so'ng (`debounce` tamoyili) serverga so'rov yuboriladi va natija o'ng maydonda ko'rsatiladi. Bu kechikish har bir tugma bosilganda so'rov yuborilishining oldini oladi va server yukini kamaytiradi.

JavaScript kodi quyidagi funksiyalarni amalga oshiradi:

- **Belgi sanoqi** — kiritilgan matnning belgilar soni real vaqtda ko'rsatiladi.
- **Tozalash tugmasi** — "✕ Tozalash" tugmasi bosilganda ikkala maydon ham tozalanadi.
- **Nusxalash tugmasi** — "📋 Nusxalash" tugmasi tarjima natijasini clipboard ga nusxalaydi; natija bo'sh bo'lsa, tugma faollashtirilmagan (`disabled`) holda qoladi.
- **Statistika** — tarjima natijasida nechta so'z tarjima qilingani va nechta so'z topilmagani ko'rsatiladi.
- **Mobil moslashma** — ekran kengligi 640 pikseldan kichik bo'lganda `@media` so'rovi yordamida ikki panel ustma-ust joylashuvga o'tadi, `dict-badge` yashiriladi.

### 3.2.4. Jinja2 shablon tizimi

Veb-interfeys Flask ning ichiga o'rnatilgan Jinja2 shablon mexanizmi asosida qurilgan. Asosiy shablon fayli `templates/index.html` da joylashgan. Ushbu faylda Flask `render_template()` funksiyasi orqali yuborilgan `dict_size` o'zgaruvchisi `{{ dict_size }}` sintaksisi yordamida sarlavha paneliga joylashtiriladi.

Statik fayllar — CSS va JavaScript — `static/` papkasida saqlanadi va Jinja2ning `{{ url_for('static', filename='...') }}` sintaksisi orqali sahifaga ulanadi. Bu yondashuv Flask ning statik fayllarni serverlash mexanizmi bilan to'liq mosdir.

---

## 3.3. Tarjima mexanizmi: lug'at yuklash, morfologik tahlil va suffiks tizimi

### 3.3.1. Umumiy arxitektura

Tarjimon dasturining markaziy komponenti `translator.py` fayli bo'lib, u barcha tarjima mantiqini o'z ichiga oladi. Ushbu fayl Flask ilovasidan `from translator import translate` ko'rinishida import qilinadi va har bir tarjima so'rovida `translate()` funksiyasi chaqiriladi.

Flask ilova (`app.py`) quyidagi vazifalarni bajaradi:

- Ilovani ishga tushirish va sozlash
- Lug'atni yuklash (`translator.py` orqali)
- Marshrut (`route`) belgilash: `/` bosh sahifa va `/translate` tarjima API si
- Jinja2 shablon yordamida HTML sahifani yaratish va foydalanuvchiga yuborish

Flask ning ishlab chiqish serveridan farqli ravishda, ishlab chiqarish muhitida dastur **Gunicorn** WSGI server orqali ishlatiladi. Gunicorn bir nechta `worker` jarayonlarini boshqaradi, bu esa bir vaqtda kelgan bir nechta so'rovni parallel qayta ishlash imkonini beradi.

### 3.3.2. Lug'at yuklash mexanizmi

Dastur ishga tushganda lug'at `output_clean.csv` faylidan bir marta yuklanadi va Python lug'ati sifatida xotiraga joylashtiriladi. Bu jarayon `_load_dictionary()` funksiyasi tomonidan bajariladi:

```python
single_dict: dict[str, str] = {}   # bir so'zli yozuvlar
phrase_dict: dict[str, str] = {}   # ko'p so'zli iboralar

def _load_dictionary(path: str) -> None:
    with open(path, newline='', encoding='utf-8') as f:
        reader = csv.DictReader(f)
        for row in reader:
            key = _normalize(row['Title'].strip().lower())
            val = row['Meaning'].strip().lower()
            if not key or not val:
                continue
            if ' ' in key:          # kalitda bo'sh joy bor — bu ibora
                phrase_dict[key] = val
            else:                   # bo'sh joy yo'q — bu bitta so'z
                single_dict[key] = val
```

Yuklash jarayonida har bir yozuv kalitida bo'sh joy bor-yo'qligiga qarab ikkita global o'zgaruvchidan biriga joylashtiriladi: bir so'zli yozuvlar `single_dict` ga, ko'p so'zli iboralar esa `phrase_dict` ga saqlanadi. Iboralarni alohida ajratish 1-bosqichdagi ko'p so'zli qidiruvni samarali bajarish imkonini beradi. Har bir tarjima so'rovida shu ikki o'zgaruvchidan foydalaniladi — ma'lumotlar bazasiga qayta murojaat qilinmaydi. Bu yondashuv tarjima tezligini sezilarli darajada oshiradi.
### 3.3.3. Besh bosqichli tarjima algoritmi

Tarjima jarayonining asosiy mexanizmi `translate()` funksiyasida amalga oshiriladi. Kiritilgan matn avval so'zlarga bo'linadi, so'ngra har bir so'z (yoki so'z birikmasi) besh bosqichli algoritm orqali qayta ishlanadi. Har bir bosqich oldingi bosqich muvaffaqiyatsiz bo'lganida ishga tushadi — agar so'z biron bosqichda tarjima qilinsa, keyingi bosqichlarga o'tilmaydi.

**1-bosqich: Ko'p so'zli iboralarni qidirish.**

Lug'atda `bari gal` (bu yoqqa kel), `bodom barmoq` (ko'rsatgich barmoq) kabi iboralar alohida kalit sifatida saqlanadi.

**2-bosqich: To'g'ridan-to'g'ri moslik (exact match).**

So'z normalizatsiya qilinib, lug'atda to'g'ridan-to'g'ri qidiriladi:

```python
if normalized in single_dict:
    return _match_case(word, single_dict[normalized])
```

Masalan, `adik` so'zi lug'atda to'g'ridan-to'g'ri topiladi va uning adabiy muqobili etik qaytariladi. Bu bosqich lug'atda mavjud bo'lgan barcha so'zlarni to'g'ri tarjima qiladi.

**3-bosqich: Fe'l morfologik tahlili.**

Agar so'z lug'atda to'g'ridan-to'g'ri topilmasa, fe'l sifatida tahlil qilinadi. Xorazm shevalarida fe'llarning turlanishi adabiy tildan sezilarli farq qiladi. `VERB_SUFFIX_MAP` jadvalida 30 ta suffiks juftligi saqlanadi — sheva qo'shimchasi va unga mos adabiy til qo'shimchasi. `VERB_ROOT_MAP` da esa 82 dan ortiq sheva fe'l ildizi — adabiy ildiz juftligi mavjud:

```python
for dialect_suffix, literary_suffix in VERB_SUFFIX_MAP.items():
    if normalized.endswith(dialect_suffix):
        root = normalized[:-len(dialect_suffix)]
        if root in VERB_ROOT_MAP:
            lit_root = VERB_ROOT_MAP[root]
            return _match_case(word, lit_root + literary_suffix)
```

Masalan, `galaman` so'zi qayta ishlanganda `-aman` qo'shimchasi ajratiladi, qolgan gal ildizi `VERB_ROOT_MAP` da `kel` sifatida topiladi va `-aman` qo'shimchasi `VERB_SUFFIX_MAP` orqali `-moqman` ga aylantiriladi; natijada `kelmoqman` qaytariladi.

**4-bosqich: Ot suffikslarini ajratish.**

Fe'l tahlili natija bermagan taqdirda, so'z ot yoki boshqa so'z turkumi sifatida tahlil qilinadi. `NOUN_SUFFIX_MAP` da qo'shimchalar tartib bo'yicha saqlanadi: uzunidan qisqasiga. Bu tartib muhim — aks holda qisqa suffiks uzoqroq suffiks bilan boshlanadigan holatda noto'g'ri ajratilishi mumkin. So'zning oxirida qo'shimcha aniqlansa, ildiz lug'atda qidiriladi; topilsa, ildizning adabiy muqobiliga adabiy tildagi mos qo'shimcha qo'shiladi:

```python
for dialect_suffix, literary_suffix in sorted(
    NOUN_SUFFIX_MAP.items(), key=lambda x: -len(x[0])
):
    if normalized.endswith(dialect_suffix):
        root = normalized[:-len(dialect_suffix)]
    if root in single_dict:
            return _match_case(word, single_dict[root] + literary_suffix)
```

**5-bosqich: O'zgartirilmay qoldirish.**

Yuqoridagi to'rt bosqichning barchasi natija bermagan taqdirda, so'z o'zgartirilmay, asl holida natijaga qo'shiladi. Bu holat statistika hisoblagichida "topilmagan so'zlar" sifatida qayd qilinadi va foydalanuvchiga ko'rsatiladi.

### 3.3.4. Tarjima API si

Flask ilovasi `/translate` marshrutida tarjima API sini ta'minlaydi. Brauzer JavaScript kodi ushbu marshrutga POST so'rovi yuboradi, so'rovda `text` parametri sifatida sheva matni jo'natiladi. Server tarjima natijasini JSON formatida qaytaradi:

```python
@app.route('/translate', methods=['POST'])
def translate():
    data = request.get_json()
    text = data.get('text', '')
    result = translate(text)
    return jsonify({'translation': result['translation'],
                    'found': result['found'],
                    'not_found': result['not_found']})
```

Javobda uchta maydon mavjud: `translation` — tarjima natijasi; `found` — tarjima topilgan so'zlar soni; `not_found` — topilmagan so'zlar soni. Brauzer bu ma'lumotlarni olib, interfeys maydonlarini yangilaydi va statistikani ko'rsatadi.

### 3.3.5. Ishlab chiqarish muhitida joylashtirish

Tarjimon dasturi Hetzner bulut serverida Ubuntu 24 operatsion tizimida joylashtirilgan. Tizim arxitekturasi quyidagi zanjirdan iborat:

**Cloudflare → Nginx → Gunicorn → Flask**

Ushbu zanjirning har bir bo'g'ini o'z vazifasini bajaradi:

**Cloudflare** — DNS boshqaruvi, DDoS himoyasi va HTTPS sertifikatini ta'minlaydi. Foydalanuvchilar brauzeridan kelgan so'rovlar birinchi navbatda Cloudflare tarmog'iga tushadi.

**Nginx** — teskari proksi (reverse proxy) vazifasini bajaradi. Nginx statik fayllarni (CSS, JavaScript) bevosita serverdan uzatadi, dinamik so'rovlarni esa Gunicorn ga yo'naltiradi. Bundan tashqari, Nginx yukni muvozanatlashtirish (load balancing) va xavfsizlik sozlamalarini boshqaradi.

**Gunicorn** — WSGI (Web Server Gateway Interface) serveri sifatida Flask ilovasi va Nginx o'rtasida ko'prik vazifasini o'taydi. Gunicorn bir nechta ishchi jarayon (`worker`) ishga tushiradi, bu esa bir vaqtda bir nechta foydalanuvchi so'rovini parallel qayta ishlash imkonini beradi. Flask ning ichki ishlab chiqarish serveri (`flask run`) bir nechta so'rovni parallel qayta ishlay olmaydi va faqat sinov muhiti uchun mo'ljallanganligi sababli, ishlab chiqarish muhitida Gunicorn'dan foydalanish zaruriy.

**Flask** — ilovaning asosiy mantiqini — lug'at yuklash, tarjima, HTML sahifalarni generatsiya qilish — bajaradi.

GitHub CI/CD integratsiyasi orqali avtomatik joylashtirish (`deploy`) tizimi ham o'rnatilgan. `master` branchga har yangi o'zgarish `push` qilinganda `deploy.sh` skripti avtomatik ishga tushadi, yangi kod serverga tortib olinadi va Gunicorn qayta ishga tushiriladi. Bu yondashuv doimiy yangilanish va xatolarni tezda tuzatish imkonini beradi.

### 3.3.6. Tarjima mexanizmining baholash natijalari

Tarjimon dasturining samaradorligini baholash uchun sinovlar o'tkazildi. Sinov uchun "Xorazm shevalari lug'ati"dan tanlangan namunaviy jumlalar ishlatildi. Natijalar quyidagicha:

- Lug'atda to'g'ridan-to'g'ri mavjud bo'lgan so'zlar uchun tarjima aniqligi yuqori.
- Fe'l qo'shimchali shakllar (`VERB_ROOT_MAP` va `VERB_SUFFIX_MAP` orqali) ko'p hollarda to'g'ri tarjima qilinadi.
- Lug'atda mavjud bo'lmagan so'zlar — asosan yangi qo'shilgan sheva so'zlari yoki mavjud bo'lmagan shakllar — o'zgartirilmay qoldiriladi; bu holat statistika orqali foydalanuvchiga aniq ko'rsatiladi.

Asosiy cheklov — tizimning lug'at chegarasiga bog'liqligi. Lug'atda mavjud bo'lmagan so'zlarni tarjima qilish imkoni yo'q. Bu cheklov kelajakda lug'atni kengaytirish orqali bartaraf etilishi mumkin. Bundan tashqari, gapning umumiy mazmunini hisobga oluvchi kontekstli tarjima ushbu tizim doirasida amalga oshirilmaydi — bu lug'at va qoidaga asoslangan yondashuvning tabiiy chegarasi hisoblanadi.