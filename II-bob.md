# **II BОB. SHEVA MATNLARINI RAQAMLASHTIRISH VA QAYTA ISHLASH**

## **2.1. Sheva lugʻatlarini raqamlashtirish muammolari va yondashuvlar**

### **2.1.1. Kirish: Raqamlashtirish zarurati**

Zamonaviy tilshunoslikda sheva lugʻatlarini raqamlashtirish - yaʼni qogʻoz shaklida mavjud boʻlgan dialektologik materiallarni kompyuter tizimlariga oʻtkazish - nafaqat arxivlash, balki jonli tilni saqlab qolishning asosiy yoʻllaridan biriga aylanib bormoqda. Oʻzbek tilshunosligi tarixida Xorazm shevalariga oid koʻplab materialar ilmiy tadqiqotlar, ekspeditsiya daftarlari va chop etilgan lugʻatlar shaklida toʻplangan. Biroq bu boylik aksari hollarda faqat kichik mutaxassis doirasiga maʼlum boʻlib qolavergan va keng jamoatchilikka yetib bormagan.

Bugungi kunda sunʼiy intellekt texnologiyalari va tabiiy tilni qayta ishlash (Natural Language Processing, NLP) sohasidagi yutuqlar tufayli sheva materiallarini raqamli formatga oʻtkazish, ularni izlash mumkin boʻlgan maʼlumotlar bazasiga aylantirish imkoni paydo boʻldi. Shu bilan birga, ushbu jarayon bir qator jiddiy texnik va lingvistik muammolarni ham oʻzida mujassamlashtiradi. Mazkur boʻlimda Xorazm shevalariga oid lugʻatlarni raqamlashtirish jarayonidagi asosiy qiyinchiliklar va ularni hal etishga qaratilgan yondashuvlar tahlil qilinadi.

### **2.1.2. Sheva materiallarining oʻziga xos xususiyatlari**

Sheva lugʻatlarini raqamlashtirish standart adabiy til lugʻatlarini raqamlashtirishdan tubdan farq qiladi. Bu farqning bir necha asosiy sababi bor.

**Yozuv va transkripsiya nomuvofiqligi.** Xorazm shevalariga oid materiallar turli davrlarda turli transkripsiya tizimlarida yozilgan. Sovet davrida kirill yozuvida toʻplangan materiallar, keyinchalik lotin alifbosiga oʻtilgach, bir qismi konvertatsiya qilinmagan holda qolgan. Bundan tashqari, dialektologlar sheva tovushlarini ifodalash uchun turli diakritik belgilar, fonologik ramzlar va xalqaro fonetik alifbo (IPA) elementlaridan foydalanganlar. Masalan, Xorazm shevalaridagi oʻziga xos unlilar - old qator lablanmagan unlilar yoki qisqa unlilar - standart alifboda mavjud boʻlmagan maxsus belgilar bilan ifodalanadi. "Xorazm shevalari lugʻati" (Norbayeva, Sadullayeva, Atabayeva, 2024)da qoʻllangan lotin yozuviga asoslangan xalqaro transkripsiya tizimi ushbu muammoni qisman hal etadi, ammo kompyuter tizimlarida bunday maxsus belgilarni qoʻllab-quvvatlash alohida texnik yechimlarni talab qiladi.

**Maʼnoning koʻp qatlamliligi.** Sheva soʻzlari koʻpincha adabiy tildagi muqobiliga toʻgʻridan-toʻgʻri mos kelmaydi. Bitta sheva soʻzi bir necha adabiy soʻz bilan ifodalanishi, yoki aksincha, maʼlum sheva iborasi adabiy tilda butun bir jumla orqali tushuntirilishi lozim boʻlishi mumkin. Bunday koʻp qatlamli maʼno munosabatlarini maʼlumotlar bazasida toʻgʻri ifodalash lugʻat tuzilmasiga nisbatan maxsus yondashuv talab qiladi.

**Nutqdan yozuvga oʻtishda yoʻqoladigan maʼlumotlar.** Sheva - avvalo ogʻzaki hodisa. Intonatsiya, urgʻu, tovush choʻziqligi va boshqa prosodik xususiyatlar koʻpincha yozma materialda aks etmaydi. Raqamlashtirish jarayonida ushbu maʼlumotlarning yoʻqolmasligi uchun audio va video yozuvlarni matnli maʼlumotlar bilan birgalikda saqlash muhim ahamiyat kasb etadi.

### **2.1.3. Asosiy texnik muammolar**

a) Optik belgilarni tanish (OCR) muammolari

Mavjud sheva lugʻatlari va dialektologik ekspeditsiya daftarlarini raqamlashtirishning dastlabki bosqichi - bu fizik hujjatlarni skanerdan oʻtkazish va matn sifatida aniqlashdan iborat. Biroq past resursli tillardagi hujjatlar uchun optik belgilarni tanish (Optical Character Recognition, OCR) tizimlari ancha past aniqlik darajasida ishlaydi. Tadqiqotlar shuni koʻrsatadiki, nooddiy skriptlar, diakritik belgilar va qoʻlyozma materiallar koʻp resursli tillarda ham OCR uchun katta qiyinchilik tugʻdiradi. Oʻzbek shevalari kabi past resursli til holatlari uchun esa bu qiyinchilik yanada chuqurlashadi.

Ushbu muammoni bartaraf etish uchun quyidagi yondashuvlar qoʻllaniladi:

- **Qoʻlda kiritish va tekshirish:** Skanerdan oʻtkazilgan sahifalar tarjima qilinib, soʻngra mutaxassis tomonidan har bir yozuv tekshirib chiqiladi. Bu usul aniq natija bersa-da, juda koʻp mehnat va vaqt talab qiladi.
- **Koʻp bosqichli OCR:** Avval umumiy OCR dasturi ishlatiladi, soʻngra maxsus lugʻat asosida xatolar tuzatiladi. Xorazm shevalarini raqamlashtirishda ham ushbu yondashuv qoʻllanilgan boʻlib, lugʻat soʻzlari alohida belgilangan transkripsiya roʻyxati orqali tekshirib borilgan.
- **Ikki skript muammmosi:** Oʻzbek tili 1992-yildan lotin yozuviga, 2023-yildan esa yangilangan lotin alifbosiga oʻtgan. Shuninga qaramay, sheva materiallarining koʻp qismi kirill yozuvida saqlanmoqda. Bu ikki tizimdagi materiallarni birgalikda qayta ishlash uchun ishonchli transliteratsiya algoritmlari ishlab chiqish zaruriyati tugʻiladi.

b) Belgilar kodlash muammolari

Unicode standartining keng tarqalishi bilan birga sheva materiallarida uchraydigan barcha maxsus belgilarning kompyuter tizimlarida toʻgʻri aks etishi muammosi hal boʻldi, deb oʻylash notoʻgʻri boʻladi. Xorazm shevalarida ishlatiladigan bir qator diakritik belgilar - masalan, qisman lablanish belgisi, orqa qator unlilarni ifodalovchi ramzlar - turli operatsion tizimlarda har xil koʻrsatilishi va maʼlumotlar bazasida notoʻgʻri saqlanishi mumkin. Bundan tashqari, eski lugʻatlarda qoʻllanilgan maxsus yozuv belgilari hozirgi Unicode jadvallarida mavjud boʻlmasligi ham muammo tugʻdiradi.

c) Maʼlumotlar tarkibini standartlashtirish

Sheva lugʻatlarini raqamlashtirish faqat soʻzlarni kiritishdan iborat emas. Har bir lugʻat yozuvi quyidagi tarkibiy qismlarni oʻz ichiga olishi lozim:

- Sheva soʻzi (transkripsiyasi bilan)
- Grammatik kategoriya (soʻz turkumi, jins, son va h.k.)
- Adabiy tildagi muqobili yoki izohi
- Qoʻllanilish namunasi (kontekst)
- Geografik tarqalish hududini koʻrsatuvchi belgi (Xorazm viloyatining qaysi tumanlarida ishlatilishi)
- Mavzu sohasiga tegishli tasnif (maishiy hayot, qishloq xoʻjaligi, hunarmandchilik va h.k.)
- Fonetik maʼlumot (kerak boʻlganda audio)

Har bir lugʻat muallifi ushbu tarkibiy qismlarni turlicha tasvirlagan. Bir tadqiqotchi geografik maʼlumotni batafsil koʻrsatgan boʻlsa, boshqasi faqat soʻz va uning qisqacha izohini qayd qilgan. Raqamlashtirish jarayonida bunday heterojen maʼlumotlarni yagona standartga keltirish muhim metodik muammoni tashkil etadi.

### **2.1.4. Lingvistik muammolar**

a) Soʻz chegarasini aniqlash

Sheva materiallarida kompozit soʻzlar (birikma soʻzlar), frazeologik birliklar va erkin soʻz birikmalari oʻrtasidagi chegara koʻpincha noaniq boʻladi. Masalan, Xorazm shevalarida uchraydigan baʼzi soʻz birikmalari adabiy tilda aynan shu maʼnoda mustaqil leksik birlik sifatida mavjud boʻlmasligi mumkin. Bunday birliklarni lugʻatda alohida yozuv sifatida kiritish yoki soʻzlar yigʻindisi sifatida izohlash masalasi leksikografik qaror talab qiladi.

b) Polisemiya va omonimiya

Koʻp maʼnoli soʻzlar (polisemiya) va shakli bir xil, ammo maʼnosi butunlay farqli soʻzlar (omonimiya) sheva lugʻatlarida alohida eʼtibor talab qiladi. Maʼlumotlar bazasini loyihalashda har bir maʼnoga alohida identifikator berish va ularni toʻgʻri bogʻlash muhim ahamiyat kasb etadi. Aks holda qidiruv funksiyasi notoʻgʻri natijalar qaytarishi mumkin.

c) Morfologik oʻzgaruvchanlik

Oʻzbek tillari agglyutinativ tuzilishga ega - yaʼni soʻzlarga turli qoʻshimchalar qoʻshib yangi grammatik shakllar hosil qilinadi. Sheva soʻzlari uchun morfologik tahlil yanada murakkablashadi, chunki shevalardagi qoʻshimchalar adabiy tildagi shakllardan farq qilishi mumkin. Masalan, Xorazm shevalarida feʼllarning hozirgi zamon qoʻshimchalari (-aman, -asan, -adi oʻrniga -maq, -mәk kabi variantlar) adabiy til bilan mutlaqo boshqacha mantiqqa ega. Raqamlashtirish jarayonida ildiz soʻz va uning grammatik shakllarini toʻgʻri bogʻlash - lemmatizatsiya masalasi - alohida algoritmik yechim talab qiladi.

d) Dialekt ichidagi farqlanish

Xorazm viloyatining oʻzida ham sheva farqlari mavjud: oʻgʻuz lahjasiga mansub hududlar (asosan viloyatning janubiy qismi) va qipchoq lahjasiga mansub hududlar (shimoliy tumanlar) bir-biridan sezilarli fonetik va leksik farqlarga ega. Lugʻatda ushbu ichki farqlanishni aks ettirish - geografik belgilash tizimi orqali - raqamlashtirishning muhim metodologik talablaridan biridir.

### **2.1.5. Raqamlashtirish yondashuvlari**

Jahon tilshunosligida sheva materiallarini raqamlashtirishga nisbatan bir necha asosiy yondashuv ishlab chiqilgan boʻlib, ular oʻzaro toʻldirib turuvchi usullardir.

1\. Oddiy elektron lugʻat (flat dictionary)

Eng sodda yondashuv - lugʻat yozuvlarini oddiy jadval shaklida, masalan CSV yoki Excel formatida raqamlashtirishdan iborat. Bu usul texnik jihatdan oson, ammo soʻzlar oʻrtasidagi munosabatlarni (sinonimiya, antonimiya, soʻz yasalishi) koʻrsatishga imkon bermaydi. Kichik hajmdagi sheva materiallarini boshlangʻich qayta ishlashda qoʻl keladi.

2\. Maʼlumotlar bazasi yondashuvi (relational database)

Relyatsion maʼlumotlar bazasi (SQL) yondashuvi sheva lugʻatlarini tuzilmalashtirilgan tarzda saqlash imkonini beradi. Har bir soʻz alohida yozuv sifatida kiritiladi, soʻzlar oʻrtasidagi munosabatlar esa bogʻliq jadvallar orqali koʻrsatiladi. Bu yondashuv keng qidiruv va filtrlash imkoniyatlarini taʼminlaydi, ammo maʼlumotlarni kiritish va boshqarish maxsus bilim talab qiladi.

3\. Ontologik va semantik yondashuv

Zamonaviy tilshunoslikda WordNet kabi ontologik tizimlardan ilhomlangan yondashuvlar ham qoʻllanilmoqda. Bu usulda soʻzlar maʼnoviy maydonlarga guruhlangan holda saqlanadi va ular oʻrtasidagi semantik munosabatlar (giponimiya, meronimi va h.k.) aniq tarzda koʻrsatiladi. Xorazm shevalarini raqamlashtirishda bunday yondashuvni toʻliq tatbiq etish hali amalga oshirilmagan, ammo kelgusida ushbu yoʻnalishda tadqiqotlar olib borish istiqbolli hisoblanadi.

4\. Multimedia korpus yondashuvi

Soʻnggi yillarda jahon dialektologiyasida matnli maʼlumotlarni audio va video yozuvlar bilan birlashtirgan multimedia korpuslari yaratish keng tarqalmoqda. Ushbu yondashuv sheva soʻzlarining talaffuzini, intonatsion xususiyatlarini va soʻzlovchi maʼlumotlarini birgalikda saqlash imkonini beradi. Xorazm shevalarini raqamlashtirishda ushbu yondashuv hozirda toʻliq tatbiq etilmagan boʻlsa-da, kelajakda audio bazalar yaratish rejasi mavjud.

5\. Oʻyin va gamifikatsiya yondashuvi (crowdsourcing)

Yaqinda ishlab chiqilgan Dia-Lingle kabi tizimlar sheva maʼlumotlarini keng jamoatchilikdan yigʻish uchun interaktiv oʻyinsimon platformalardan foydalanadi. Bu yondashuv asosan ona tili soʻzlovchilarini ilmiy jarayonga faol jalb qilish imkonini beradi va maʼlumotlar bazasini tezda kengaytirish uchun samarali usul hisoblanadi. Xorazm shevalarini raqamlashtirishda mahalliy aholi, oʻqituvchilar va sheva soʻzlovchilarini shunga oʻxshash platforma orqali jalb etish istiqbolli yoʻnalish boʻlib koʻrinadi.

2.1.6. Oʻzbek va turkiy tillar uchun xos muammolar

Oʻzbek tili va uning shevalari boshqa past resursli turkiy tillar bilan umumiy muammolarni baham koʻradi. Tadqiqotlar shuni koʻrsatadiki, Markaziy Osiyo turkiy tillari - qozoq, oʻzbek, qirgʻiz, turkman - NLP sohasida maʼlumot tanqisligi, cheklangan lingvistik resurslar va texnologik rivojlanish nuqtai nazaridan jiddiy qiyinchiliklarga duch kelmoqda. Oʻzbek tili interneti uchun ham resurs cheklanganligi kuzatiladi: internetdan toʻplangan maʼlumotlar koʻpincha rus tilida boʻlib, oʻzbek tilidagi kontent nisbatan kam.

Bu holat sheva materiallariga nisbatan yanada chuqurlashadi. Agarda adabiy oʻzbek tilining oʻzi ham past resursli deb hisoblansa, Xorazm shevalari - bu tilning ichida yanada past resursli pastki tizim - deyarli texnologik eʼtibordan chetda qolgan. Shuning uchun Xorazm shevalarini raqamlashtirishda jahon tajribasidan foydalanish bilan birga, oʻzbek tili va sheva materiallarining oʻziga xos xususiyatlarini hisobga olgan mahalliy yechimlar ishlab chiqish zarur.

Bundan tashqari, oʻzbek tili yozuv tizimining bir necha bor oʻzgarishi - arab yozuvidan kirill yozuviga (1940), kirill yozuvidan lotin yozuviga (1992), soʻngra yangilangan lotin alifbosiga (2023) - tarixiy sheva materiallarini raqamlashtirishda qoʻshimcha qiyinchilik tugʻdiradi. Turli davrlarda toʻplangan materiallar turli yozuv sistemalarida boʻlib, ularni bir formatga keltirish transliteratsiya algoritmlarini ishlab chiqishni talab qiladi.

### **2.1.7. Xorazm shevalarini raqamlashtirishda qoʻllanilgan yondashuv**

Ushbu diplom ishida Xorazm shevalarini raqamlashtirishning amaliy tajribasidan kelib chiqib, bir necha bosqichli yondashuv qabul qilingan.

**Birinchi bosqich - manba materiallarini tayyorlash.** "Xorazm shevalari lugʻati" (2024)ning sahifalari skanerdan oʻtkazilgan va OCR texnologiyasi yordamida matn ajratib olingan. Maxsus transkripsiya belgilarini qayta ishlash uchun dastlabki belgilarni normallashtirish (normalizatsiya) funksiyasi ishlab chiqilgan. Bunda turli manbalarda uchraydigan diakritik belgilar (ä, ö, ü kabi) ularning sodda o'zbek lotin muqobillariga o'tkazilgan — bu yondashuv dasturni standart klaviaturada matn teradigan foydalanuvchilar uchun qulay qiladi.

**Ikkinchi bosqich - maʼlumotlarni tozalash va standartlashtirish.** Avtomatik tarzda ajratib olingan lugʻat yozuvlari qoʻlda tekshirilgan. Geografik izohlar (mahalla nomi, qishloq nomi va h.k.) alohida maydonlarga ajratilgan. Raqamli yoki ketma-ket koʻrsatilgan koʻp maʼnoli soʻz izohlari qayta tarkiblashtirilgan.

**Uchinchi bosqich - morfologik tahlil va tarjima mexanizmini yaratish.** Sheva soʻzlarini adabiy oʻzbek tiliga tarjima qilish uchun ildiz soʻz va qoʻshimchalarni ajratuvchi morfologik tahlilchi - lemmizator - ishlab chiqilgan. Feʼl ildizlari va sheva qoʻshimchalari alohida lugʻat jadvallari sifatida saqlanib, tarjima jarayonida ular ketma-ket qoʻllaniladi.

**Toʻrtinchi bosqich - foydalanuvchi interfeysi.** Raqamlashtirilgan lugʻat materiallariga qulay kirish imkonini beruvchi interaktiv tarjimon dasturi yaratilgan. Ushbu dastur soʻz qidirish, morfologik tahlil qilish va sheva matnini adabiy tilga tarjima qilish funksiyalarini oʻz ichiga oladi.


## 2.2. Sheva manbalaridan lug'at ma'lumotlarini to'plash va tizimlashtirish

### 2.2.1. Manba materiallarining tavsifi

Sheva lug'atini raqamli tarjimon dasturiga aylantirishning dastlabki va eng muhim bosqichi — manba materiallarini to'plash va ularni tizimli qayta ishlashdir. Ushbu diplom ishida asosiy manba sifatida Norbayeva, Sa'dullayeva va Atabayeva tomonidan 2024-yilda nashr etilgan "Xorazm shevalari lug'ati" (1-jild) tanlangan. Ushbu tanlovning asosiy sababi shundaki, mazkur lug'at Xorazm shevalarini lotin yozuviga asoslangan xalqaro transkripsiya tizimida qayd etgan, hududiy belgilarni (qaysi tumanda qo'llanishi) izchil ko'rsatgan va 2024-yil holatiga ko'ra eng yangi ilmiy manbalar qatoriga kiradi.

Biroq bitta manba bilan cheklanish lug'at hajmining etarlicha keng bo'lmasligiga sabab bo'lardi. Shu sababli qo'shimcha manbalar ham jalb qilingan:

**Asosiy manba** — "Xorazm shevalari lug'ati" (Norbayeva Sh., Sa'dullayeva N., Atabayeva M., 2024). Ushbu lug'at diakritik belgilar yordamida fonetik jihatdan aniq ifodalangan sheva so'zlarini, ularning adabiy tildagi muqobillarini va qo'llanish hududlarini o'z ichiga oladi. Lug'atning sahifalari skanerdan o'tkazilib, OCR (optik belgilarni tanish) texnologiyasi yordamida matn sifatida ajratib olingan.

**Qo'shimcha manba 1** — Xorazm shevasi leksikasini o'z ichiga olgan Excel formatidagi jadval. Ushbu jadval oldingi yillarda olib borilgan dialektologik tadqiqotlar va ekspeditsiyalar asosida to'plangan materiallardan iborat bo'lib, taxminan 1340 ta yozuvni o'z ichiga oladi. Lotin yozuvida tuzilgan bu jadval asosiy manbadan farqli diakritik tizimda bo'lgani sababli, uni birlashtirish jarayonida maxsus normalizatsiya talab qilingan.

**Qo'shimcha manba 2** — dasturchi S. Ernazarov tomonidan yaratilgan "Xorazmcha" mobil ilovasining lug'at ma'lumotlari. Ushbu ilova (xorazmcha.uz) o'zbek dialektologiyasida sheva lug'atini raqamli ilovaga aylantirgan birinchi tajribalardan biri sifatida ahamiyatlidir. Biroq ilovadagi ma'lumotlar kirill yozuvida bo'lgani va diakritik belgilardan foydalanilmagani sababli, ushbu manba ham lotin yozuviga o'tkazilish va normalizatsiya qilinishni talab qilgan.

Uchta manbadan olingan ma'lumotlar birlashtirish jarayonida "asosiy manba ustunligi" tamoyiliga rioya qilingan: bitta so'z uchun turli manbalarda turli muqobil berilgan taqdirda, "Xorazm shevalari lug'ati" (2024)dagi talqin mezon sifatida qabul qilingan.

### 2.2.2. OCR yordamida ma'lumot ajratib olish

"Xorazm shevalari lug'ati"ning bosma sahifalaridan matn ajratib olish jarayoni ushbu ishning texnik jihatdan eng murakkab qismi bo'ldi. Bosma lug'atda qo'llanilgan xalqaro transkripsiya belgilari — masalan, *ā*, *ö*, *ü*, *ş*, *ç*, *ğ* kabi diakritik belgilar — standart OCR tizimlari uchun qiyinchilik tug'diradi, chunki bu belgilar oddiy lotin alifbosidan tashqarida joylashadi.

Ushbu muammoni bartaraf etish uchun Hugging Face platformasida joylashgan **LightOnOCR-2-1B** modeli tanlandi. Ushbu model standart Tesseract va boshqa umumiy OCR vositalariga nisbatan ko'p tillilik va noodatiy belgilarni tanishda ustunlik ko'rsatdi. Model Google Colab muhitida Nvidia T4 GPU yordamida ishga tushirildi. Xotira yetarli bo'lmasligi muammolarini oldini olish uchun sahifalar pastroq masshtab parametri bilan qayta ishlandi va har bir sahifadan so'ng CUDA xotirasi tozalandi.

OCR jarayoni quyidagi tartibda amalga oshirildi:

**1-qadam — Tayyorlov.** Lug'at sahifalari yuqori sifatli skaner yordamida raqamli formatga o'tkazildi. Sahifalar PDF yoki PNG formatida saqlandi.

**2-qadam — Model yuklash va ishga tushirish.** LightOnOCR-2-1B modeli Colab muhitiga yuklanib, har bir sahifa alohida qayta ishlandi. Natijalar Markdown formatida saqlandi.

**3-qadam — Natijani tekshirish.** Avtomatik ajratib olingan matn diakritik belgilar va lug'at tuzilishi nuqtai nazaridan qo'lda tekshirildi. Noto'g'ri tanilgan belgilar — masalan, *ā* o'rnida *a*, *ö* o'rnida *o* yozilganda — qo'lda tuzatildi.

**4-qadam — Lug'at yozuvlarini ajratish.** Har bir sahifadagi matndan alohida lug'at yozuvlari ajratib olindi. "Xorazm shevalari lug'ati"da har bir yozuv quyidagi tuzilmada keltirilgan:

```
sheva_so'zi [adabiy_talaffuz] – adabiy_muqobil; izoh (hudud).
Misol jumla.
```

Ushbu tuzilmadan foydalanib, Python tilida maxsus ajratish skripti yozildi. Skript to'rtburchak qavslar `[]` ichidagi adabiy talaffuzni, tire `–` dan keyingi adabiy muqobilni va qavs ichidagi hududiy belgilarni (Urg., Xv., Shvt. va h.k.) alohida ustunlarga ajratdi.

### 2.2.3. Ma'lumotlarni tozalash va normalizatsiya

Xom OCR natijalaridan foydalanish mumkin bo'lgan lug'at yozuvlarini olish uchun bir necha bosqichli tozalash va normalizatsiya jarayoni o'tkazildi. Bu jarayon dasturiy vosita sifatida Python va uning `csv` kutubxonasidan foydalangan holda amalga oshirildi.

**Diakritik belgilarni sodda lotin yozuviga o'tkazish.** Manba lug'atlarda qo'llanilgan transkripsiya tizimlari bir-biridan farq qilardi: "Xorazm shevalari lug'ati"da ä, ö, ü, ş, ç, ğ kabi xalqaro transkripsiya belgilari ishlatilgan edi. Ushbu nomuvofiqlikni bartaraf etish va, eng muhimi, dasturni amaliy foydalanish uchun qulay qilish maqsadida ongli dizayn qarori qabul qilindi: barcha diakritik belgilar o'zlarining sodda o'zbek lotin muqobillariga o'tkazildi (masalan, ä → a, ö → o, ü → u, ş → sh, ç → ch, ğ → g'). Bu qarorning asosiy sababi shundaki, bugungi kunda Xorazm shevasida so'zlashuvchilarning aksariyati matn yozishda diakritik belgilardan foydalanmaydi — ular standart o'zbek lotin klaviaturasidan foydalanadi. Agar lug'at diakritik belgilarda saqlanganida, foydalanuvchi ä yoki ş kabi belgilarni odatdagi klaviaturada tera olmagani sababli dasturdan amalda foydalana olmas edi. Shu tariqa diakritik belgilarni soddalashtirish — ilmiy jihatdan aniq manba bilan amalda ishlatib bo'ladigan vosita o'rtasidagi ko'prik vazifasini o'tadi.

**Bo'sh va takroriy yozuvlarni o'chirish.** Birlashtirish jarayonida bir xil sheva so'zi turli manbalarda uchrab, dublikatlar paydo bo'ldi. `csv_clean.py` skripti orqali barcha yozuvlar alifbo tartibida saralanib, bir xil sheva so'ziga tegishli yozuvlar aniqlanib, kamroq ma'lumotli yozuv o'chirildi.

**Registrni standartlashtirish.** Barcha lug'at muqobillari kichik harfda saqlanishi belgilandi. Bu orqali qidiruvda registr xatolarining ta'siri minimallashtirildi. Lekin so'zning gaplardagi haqiqiy registrini saqlash uchun `_match_case()` funksiyasi ham ishlab chiqildi — u kiritilgan so'zning bosh harfini tanib, muqobilini ham xuddi shu qoida asosida formatlaydi.

**Manba ustunligini ta'minlash.** `merge_dicts.py` skripti orqali uchta manba birlashtirildi. Ushbu skript har bir so'zni avval asosiy manbadan (output.csv) qidiradi; topilmagan taqdirda qo'shimcha manbadan (fromexcel.csv) oladi. Bu yondashuv ilmiy jihatdan eng ishonchli manba — "Xorazm shevalari lug'ati" (2024) — ning ustunligini kafolatlaydi.

Tozalash jarayonlari yakunida lug'at taxminan 3486 ta yozuvni o'z ichiga olgan holda `output_clean.csv` faylida saqlandi. Har bir yozuv ikki asosiy ustundan iborat: `sheva` (Xorazm sheva so'zi) va `adabiy` (adabiy o'zbek tili muqobili).

### 2.2.4. Ma'lumotlarni tizimlashtirish tamoyillari

Lug'at ma'lumotlarini tizimlashtirish — ya'ni turli manbalardan olingan heterojen ma'lumotlarni yagona izchil tuzilmaga keltirish — bu ish doirasidagi eng muhim metodologik qarorlardan birini tashkil etdi.

Tizimlashtirishda quyidagi tamoyillarga rioya qilindi:

**Bitta kalit — bitta yozuv tamoyili.** Lug'atda har bir sheva so'zi (kalit) uchun bitta yozuv saqlanadi. Ko'p ma'noli so'zlar uchun muqobil matnda vergul orqali ajratilgan holda yoziladi: masalan, *äkä* so'zining muqobili `aka, ota` tarzida beriladi.

**Ko'p so'zli iboralar alohida yozuv sifatida.** Xorazm shevalarida uchraydigan ko'p so'zli sheva iboralari — masalan, *sırt berdi*, *äyqaş-uyqaş* — alohida kalit sifatida lug'atga kiritildi. Tarjima mexanizmida ko'p so'zli iboralar birinchi navbatda qidiriladi, shundan keyingina alohida so'zlar uchun qidirish amalga oshiriladi.

**Manbaga ishora saqlanishi.** Har bir yozuvning qaysi manbadan olinganligini bilish texnik takomillashtirish va kelajakda audit qilish uchun muhim. Shu sababli birlashtirish jarayonida har bir yozuvga manba belgisi (`source` ustuni) qo'shildi: `norbayeva2024`, `fromexcel`, `xorazmcha` kabi qiymatlar bilan.

**Fonetik jihatdan o'xshash variantlarni birlashtirish.** Bir xil so'zning turli imloviy variantlari — masalan, *dîlânmaq* va *dilonmoq* — bir yozuv ostida birlashtirildi. Normalizatsiya funksiyasi bu variantlarni qidiruv jarayonida ham bir xil deb qabul qiladi.

---

## 2.3. Shevaga oid mavjud dasturiy yechimlar va ularning tahlili

### 2.3.1. Kirish: Tahlil zarurati

Yangi dasturiy yechim yaratishdan avval mavjud analoglarni o'rganish va ularning kuchli hamda zaif tomonlarini tahlil qilish metodologik jihatdan muhimdir. Bunday tahlil yangi tizimning nima uchun zarurligini asoslab beradi, mavjud kamchiliklarni bartaraf etish uchun qanday yondashuvlar qo'llanishi mumkinligini belgilaydi va oxirgi mahsulotning uqubat qilingan xususiyatlarini shakllantirishga yordam beradi. Ushbu bo'limda Xorazm shevasi leksikasiga tegishli mavjud dasturiy yechimlar — veb-ilovalar, mobil dasturlar va lug'at saytlari — ko'rib chiqiladi va ulardagi asosiy cheklovlar baholanadi.

### 2.3.2. "Xorazmcha" mobil ilovasi tahlili

Hozirda mavjud bo'lgan Xorazm shevasi bilan bevosita bog'liq dasturiy yechimlar ichida dasturchi S. Ernazarov tomonidan ishlab chiqilgan **"Xorazmcha"** mobil ilovasi eng diqqatga sazovor hisoblanadi. Ushbu ilova App Store va Google Play do'konlarida bepul tarqatilgan bo'lib, Xorazm shevasi so'zlarini qidirish va adabiy muqobilini ko'rish imkonini beradi.

Ilovaning kuchli tomonlari quyidagilardan iborat: birinchidan, foydalanuvchilarga oflayn rejimda, internetga ulanmasdan ishlash imkonini berishi; ikkinchidan, kirill va lotin yozuvlarini qo'llab-quvvatlashi; uchinchidan, qidiruv funksiyasining mavjudligi; to'rtinchidan, ilovaga yangi so'zlarni qo'shish imkonini beruvchi administrativ panel mavjudligi.

Biroq ilova bir qator muhim cheklovlardan xoli emas. Eng asosiy kamchilik shundaki, ilovada diakritik belgilardan foydalanilmagan. Natijada bir-biridan fonetik jihatdan farq qiluvchi so'zlar bitta yozuv ostida birlashtirib yuborilgan yoki talaffuzi noaniq holda qoldirilgan. Masalan, *ā* (cho'ziq a) va *a* (qisqa a) farqini ilovadagi yozuvlardan aniqlash mumkin emas. Bu holat leksikografik aniqlik nuqtai nazaridan jiddiy kamchilik hisoblanadi.

Bundan tashqari, ilova so'z birikmalarini yaxlit birlik sifatida qidira olmaydi — faqat alohida so'zlar qidiriladi. Morfologik tahlil funksiyasi yo'q: agar foydalanuvchi so'zning qo'shimcha bilan kelgan shaklini — masalan, *dîlânmaqda* — kiritsa, ilova natija topa olmaydi. Shuningdek, geografik hududiy belgilar ham ko'rsatilmagan, ya'ni so'zning Xorazm viloyatining qaysi tumanida qo'llanishi ilovadan bilib bo'lmaydi.

Yakunlovchi baho sifatida aytish mumkinki, "Xorazmcha" ilovasi Xorazm shevalarini raqamli sohaga olib kirishda muhim birinchi qadam bo'ldi. Biroq u lingvistik aniqlik va texnik funktsionallik nuqtai nazaridan to'liq yechim bo'la olmaydi.

### 2.3.3. GitHub'dagi "Translate-Uzbek-Khorazm" loyihasi tahlili

IlhomJabborov tomonidan GitHub'da joylashtirilgan **"Translate-Uzbek-Khorazm"** ochiq kodli loyiha Xorazm shevasidan o'zbek adabiy tiliga va aksincha tarjima qiluvchi veb-sayt sifatida taqdim etilgan. Loyiha GitHub'dagi tavsifga ko'ra, "istalgan o'zbekcha yoki xorazmcha so'zni yozsangiz shu so'zni adabiy tilda yoki xorazm shevasida chiqarib beradi" va "hozirgi paytda 100 dan ortiq so'z kiritilgan".

Ushbu loyihaning asosiy afzalligi — ochiq kod bo'lganligi, ya'ni manba kodi bepul foydalanish uchun mavjud. Bu boshqa ishlab chiquvchilarga loyihadan ilhomlana olish yoki kod qismlaridan qayta foydalanish imkonini beradi.

Biroq loyihaning jiddiy cheklovi uning lug'at hajmi bilan bog'liq. 100 dan ortiq so'z Xorazm shevasining boy leksikasini ifodalash uchun mutlaqo yetarli emas — bu hajm ushbu diplom ishidagi 3486 ta yozuvdan taxminan 35 marta kam. Buning ustiga, loyihada morfologik tahlil, ko'p so'zli iboralar qidirish yoki suffiksni ajratish kabi funksiyalar ko'zda tutilmagan. Loyiha holatini ko'rsatuvchi ma'lumotlar cheklanganligi sababli, so'zlar qanday mezon asosida tanlanganini va ularning qanchalik darajada tekshirilganini baholash ham qiyin.

### 2.3.4. Umumiy tarjimon tizimlari va ularning shevalarga munosabati

O'zbek tili uchun mo'ljallangan umumiy tarjimon tizimlar — Google Translate, Yandex.Translate va boshqalar — Xorazm shevasi so'zlarini tarjima qilishda qat'iy cheklovlarga ega. Bu tizimlar o'zbek adabiy tilida yozilgan matnlarni boshqa tillarga tarjima qilish uchun optimallashtirilgan va sheva leksikasini deyarli taniy olmaydi.

Masalan, *äldin* so'zini (Xorazm shevasida "oldin" maʼnosida qo'llanadigan) Google Translate'ga kiritilganda tizim natija topa olmaydi yoki noto'g'ri tarjima beradi. Xuddi shunday, *ällî* (ellik) yoki *dîlânmaq* (yig'lamoq maʼnosidagi feʼl) kabi so'zlar ham bu tizimlar uchun "noma'lum" sifatida baholanadi. Bu holat tabiiy — chunki umumiy tarjimon tizimlar keng ko'lamli adabiy matnlar asosida o'qitilgan, sheva materiallarini o'z ichiga olmaydi.

Elektron lug'atlar va tarjima ilovalari tahlili bo'yicha o'zbek va turk tillari misolida olib borilgan tadqiqotlar shuni ko'rsatadiki, "kitob" lug'atlaridan elektron lug'atlarga o'tish nafaqat qulaylikni oshiradi, balki yangilash, to'ldirish va qidiruv imkoniyatlarini ham sezilarli darajada kengaytiradi. Biroq bu tadqiqotlarda sheva lug'atlarini elektron shaklga o'tkazish masalasi alohida ko'rib chiqilmagan — bu sohada o'zbek tilshunosligida katta bo'shliq mavjud.

### 2.3.5. Mavjud yechimlarning umumiy kamchiliklari

Tahlil qilingan barcha mavjud dasturiy yechimlarning umumiy kamchiliklarini quyidagicha jamlash mumkin:

**Lug'at hajmining chegaralanganligi.** Mavjud ilovalar Xorazm shevasi leksikasining faqat kichik bir qismini qamrab olgan. Sheva so'zlarining to'liq qamrovini ta'minlash uchun bir necha manbadan ma'lumot to'plash, tozalash va birlashtirish zarurligi ko'zga tashlanadi.

**Morfologik tahlilning yo'qligi.** Hech bir mavjud yechim sheva so'zlarini morfologik jihatdan tahlil qila olmaydi. Ya'ni, foydalanuvchi sheva so'zini qo'shimcha bilan birga kiritsa — *dîlânmaqda*, *ällîdan*, *äkäm* kabi — tizimlar natija bermaydi. Shu sababli ildiz so'zni ajratuvchi va qo'shimchalarni alohida tahlil qiluvchi mexanizm yaratish zaruriyati ayon bo'ladi.

**Diakritik belgilar bilan ishlashdagi muammolar.** Xorazm shevasi tovush tizimini to'liq ifodalash uchun transkripsion diakritik belgilar zarur. Mavjud ilovalar bu belgilarni ko'pincha e'tiborsiz qoldiradi, bu esa fonetik aniqlik va leksikografik ishonchlilikka zarar yetkazadi.

**Matn darajasida tarjimaning yo'qligi.** Mavjud yechimlar faqat alohida so'zlarni qidirish imkonini beradi. Bir nechta sheva so'zidan iborat butun gapni tarjima qilish — so'zma-so'z hatto bo'lsa-da — hech bir mavjud tizimda ko'zda tutilmagan.

**Veb-sayt ko'rinishida ishlashning cheklanganligi.** Mavjud yechimlarning aksariyati mobil ilovalar sifatida ishlab chiqilgan. Kompyuter brauzeri orqali qulay foydalanish imkoniyatini ta'minlovchi maxsus veb-interfeys esa deyarli yo'q.

### 2.3.6. Tahlil xulosasi va yangi yechim zarurati

Mavjud dasturiy yechimlarning ko'rib chiqilishi shuni ko'rsatadiki, Xorazm shevasi manbalarini to'liq qamrab olgan, morfologik tahlilni amalga oshira oladigan, diakritik belgilar bilan to'g'ri ishlaydigan va foydalanuvchi uchun qulay veb-interfeys taqdim etadigan yechim hali yaratilmagan.

Ushbu diplom ishining asosiy maqsadi — xuddi ana shu bo'shliqni to'ldirish. III bobda batafsil tavsiflanadigan tarjimon dastur quyidagi asosiy xususiyatlar bilan mavjud analoglardan tubdan farqlanadi: 3486 ta yozuvli keng lug'at bazasi; besh bosqichli tarjima algoritmi (ko'p so'zli iboralar, to'g'ri moslik, feʼl morfologik tahlili, ot suffikslari ajratish, o'zgartirilmay qoldirish); barcha belgilar variantlarini bir xil deb qaraydigan normalizatsiya tizimi; va Cloudflare – Nginx – Gunicorn – Flask zanjiri orqali tarqatilgan ishonchli veb-platforma.

Shu tarzda ushbu ish nafaqat mustaqil tadqiqot mahsuli, balki Xorazm shevalarini raqamli texnologiyalar bilan boyitishning keyingi bosqichi uchun amaliy poydevor hamdir.
