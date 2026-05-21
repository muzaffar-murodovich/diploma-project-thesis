# KIRISH

## Mavzuning dolzarbligi

Hozirgi davrda axborot texnologiyalarining jadal rivojlanishi madaniy va lingvistik merosni saqlash hamda kelajak avlodlarga yetkazishning yangi imkoniyatlarini ochib bermoqda. Oʻzbekiston Respublikasi Prezidentining 2019-yil 21-oktabrdagi "Oʻzbek tilining davlat tili sifatidagi nufuzi va mavqeyini tubdan oshirish chora-tadbirlari toʻgʻrisida"gi farmonida ona tilini har tomonlama oʻrganish, uning lugʻat boyligini saqlash va rivojlantirish, milliy madaniy merosning ajralmas qismi sifatida tilning hududiy variantlari — shevalarga eʼtibor qaratish vazifalari qoʻyilgan. Bu vazifalarni zamonaviy raqamli vositalar yordamida hal qilish dolzarb ilmiy va amaliy yoʻnalishlardan birini tashkil etadi.

Oʻzbek tilining boy va rang-barang dialektologik tizimida Xorazm shevalari oʻziga xos oʻrin egallaydi. Mintaqada oʻgʻuz va qipchoq lahjalarining yonma-yon yashashi, qadimiy turkiy qatlamlarning saqlanib qolganligi, fonetik va leksik darajadagi oʻziga xos belgilarning mavjudligi — bularning barchasi Xorazm shevalarini umumturkiy tilshunoslik nuqtai nazaridan ham, oʻzbek dialektologiyasi nuqtai nazaridan ham nodir tadqiqot obyektiga aylantiradi.

Biroq, urbanizatsiya, ommaviy axborot vositalarining keng tarqalishi, aholining migratsiyasi va umumiy taʼlim tizimining adabiy tilni ustun darajaga olib chiqishi natijasida shevalar tildagi oʻrnini asta-sekin yoʻqotmoqda. Yoshlar nutqida sheva belgilari kamayib, koʻplab original sheva soʻzlari isteʼmoldan chiqib bormoqda. Tilshunoslar bu jarayonni "sheva inqirozi" sifatida baholamoqda. Shu sababli sheva merosini ilmiy asosda qayd etish, raqamli formatda saqlash va keng jamoatchilikka yetkazish bugungi kunning kechiktirib boʻlmaydigan masalalaridan biriga aylangan.

Hozirgi vaqtda Xorazm shevasiga oid mavjud raqamli yechimlar — "Xorazmcha" mobil ilovasi va GitHub'dagi "Translate-Uzbek-Khorazm" loyihasi — muhim birinchi qadamlar boʻlsa-da, ular lugʻat hajmining kichikligi, morfologik tahlilning yoʻqligi, fonetik diakritik belgilar bilan ishlay olmasligi va matn darajasida tarjimaning cheklanganligi singari jiddiy kamchiliklardan xoli emas. 2024-yilda Urganch davlat universiteti olimlari tomonidan nashr etilgan "Xorazm shevalari lugʻati" (1-jild) ilmiy jihatdan ishonchli, xalqaro transkripsiyaga asoslangan keng qamrovli manba boʻlib, uni raqamli formatga oʻtkazish va veb-platforma orqali foydalanuvchilarga yetkazish dolzarb vazifaga aylangan.

## Muammoning qoʻyilishi

Yuqorida bayon etilgan holatdan kelib chiqib, ushbu tadqiqotda quyidagi asosiy ilmiy-amaliy muammo qoʻyiladi: **Xorazm shevasi lugʻat materiallarini raqamli formatga oʻtkazish va ular asosida sheva matnini adabiy oʻzbek tiliga avtomatik tarjima qila oluvchi veb-ilova ishlab chiqish**. Bu muammoni hal qilish jarayonida bir nechta texnik qiyinchiliklar yuzaga keladi: bosma lugʻatdagi xalqaro transkripsiya belgilarini OCR yordamida saqlab qolish, turli manbalardan olingan maʼlumotlarni normalizatsiya qilish va birlashtirish, sheva soʻzlarining morfologik shakllarini avtomatik tahlil qilish, hamda foydalanuvchi uchun qulay va tez ishlaydigan veb-interfeys taqdim etish.

## Tadqiqotning maqsadi va vazifalari

**Tadqiqotning asosiy maqsadi** — Xorazm shevasidan adabiy oʻzbek tiliga oʻgirib beruvchi veb-ilova ishlab chiqish hamda buning uchun zarur boʻlgan lugʻat bazasini ilmiy ishonchli manbalar asosida shakllantirishdir.

Ushbu maqsadga erishish uchun quyidagi vazifalar belgilandi:

1. Xorazm shevalarining shakllanish tarixi, tarqalish hududlari va fonetik-leksik-grammatik xususiyatlarini ilmiy adabiyotlar asosida tahlil qilish;
2. Xorazm sheva lugʻatchiligining rivojlanish bosqichlarini va mavjud asosiy lugʻat manbalarini oʻrganish;
3. Sheva matnlarini raqamlashtirishning nazariy va metodologik masalalarini, mavjud yondashuvlarning kuchli va zaif tomonlarini aniqlash;
4. Lugʻat manbalarini OCR texnologiyasi yordamida raqamli formatga oʻtkazish, tozalash, normalizatsiya qilish va birlashtirish;
5. Mavjud dasturiy yechimlarni tahlil qilib, ulardagi cheklovlarni aniqlash va yangi ilovaning farqlovchi xususiyatlarini belgilash;
6. CSV formatidagi lugʻat bazasi asosida tarjima mexanizmini va morfologik tahlilchini Python tilida loyihalash;
7. Foydalanuvchiga qulay veb-interfeys (UI/UX) ishlab chiqish va uni Flask freymvorki asosida amalga oshirish;
8. Ilovani Cloudflare, Nginx va Gunicorn zanjiri orqali ishlab chiqarish muhitida joylashtirish hamda GitHub CI/CD integratsiyasini taʼminlash;
9. Axborot texnologiyalari sohasidagi mutaxassislar uchun hayot faoliyati xavfsizligi masalalarini koʻrib chiqish.

## Tadqiqot obyekti va predmeti

**Tadqiqot obyekti** — Xorazm shevalari, ularning lugʻat fondi va shu shevalarni raqamlashtirish boʻyicha mavjud dasturiy yechimlar.

**Tadqiqot predmeti** — Xorazm sheva soʻzlarini adabiy oʻzbek tiliga avtomatik tarzda oʻgirib beruvchi veb-ilovani loyihalash va amalga oshirish jarayoni, shu jumladan lugʻat bazasini shakllantirish, morfologik tahlil algoritmlarini ishlab chiqish va tarqatilgan veb-arxitekturani qurish masalalari.

## Ilmiy yangiligi

Ushbu bitiruv malakaviy ishining ilmiy yangiligi quyidagilardan iborat:

- birinchi marta 2024-yilda nashr etilgan "Xorazm shevalari lugʻati" (1-jild) bosma manbasi OCR texnologiyasi (LightOnOCR-2-1B modeli) yordamida toʻliq raqamlashtirildi va xalqaro transkripsiya belgilari saqlangan holda CSV bazasiga aylantirildi;
- Xorazm shevasi uchun maxsus loyihalangan **besh bosqichli tarjima algoritmi** ishlab chiqildi: koʻp soʻzli iboralar qidirish, toʻgʻridan-toʻgʻri moslik, feʼl morfologik tahlili, ot suffikslarini ajratish va topilmagan soʻzlarni saqlab qolish;
- shevadagi feʼllarni adabiy tilga tarjima qilish uchun maxsus `VERB_ROOT_MAP` va `VERB_SUFFIX_MAP` tuzilmalari yaratildi;
- diakritik belgilarning turli yozuv variantlarini bir xil deb qabul qiluvchi normalizatsiya tizimi ishlab chiqildi;
- mavjud analoglardan farqli ravishda, lugʻat hajmi **3486 ta yozuvgacha** kengaytirilib, matn darajasidagi tarjimani amalga oshira oluvchi yagona veb-yechim taqdim etildi.

## Amaliy ahamiyati

Ishning amaliy ahamiyati shundan iboratki, yaratilgan veb-ilova foydalanuvchilarga ochiq xizmat sifatida taqdim etilgan boʻlib, talabalar, oʻqituvchilar, tilshunoslar, mahalliy tarix va madaniyat ishqibozlari hamda Xorazm shevasi bilan qiziquvchi har qanday foydalanuvchi undan internet orqali bevosita foydalanishi mumkin. Ilova oddiy soʻzlardan tortib qoʻshimcha bilan kelgan morfologik shakllargacha tahlil qila oladi va lugʻatdagi 3486 ta yozuv asosida adabiy tildagi muqobilini taqdim etadi. Ishlab chiqilgan dasturiy yechim shu bilan birga sheva merosini saqlashning amaliy modeliga aylanib, boshqa oʻzbek shevalari (Toshkent, Buxoro, Samarqand va boshqalar) uchun ham oʻxshash ilovalar yaratishda metodologik asos boʻlib xizmat qilishi mumkin.

## Tadqiqot uslublari

Tadqiqot jarayonida quyidagi ilmiy va amaliy uslublardan foydalanildi:

- **lingvistik tahlil uslubi** — Xorazm shevalarining fonetik, leksik va grammatik xususiyatlarini oʻrganishda;
- **qiyosiy-tarixiy uslub** — Xorazm shevalarini umumturkiy tillar va adabiy oʻzbek tili bilan taqqoslashda;
- **manbashunoslik uslubi** — mavjud sheva lugʻatlari va dialektologik tadqiqotlarni tahlil qilishda;
- **OCR va matnni qayta ishlash uslublari** — bosma lugʻatni raqamli formatga oʻtkazishda;
- **dasturiy injiniring uslublari** — veb-ilovani loyihalash, ishlab chiqish va joylashtirish jarayonida (modulli arxitektura, versiya boshqaruvi Git, CI/CD avtomatlashtirish);
- **qiyosiy tahlil uslubi** — mavjud raqamli yechimlarning afzallik va kamchiliklarini baholashda.

## Ishning tuzilishi

Bitiruv malakaviy ishi kirish, toʻrt asosiy bob, xulosa, foydalanilgan adabiyotlar roʻyxati va ilovalardan iborat.

**I bob** — "Xorazm shevalari: tarixiy-lingvistik tahlil" — shevalarning shakllanish tarixini, tarqalish hududlarini, fonetik-leksik-grammatik xususiyatlarini hamda lugʻatchilik tadqiqotlarini koʻrib chiqadi.

**II bob** — "Sheva matnlarini raqamlashtirish va qayta ishlash" — sheva lugʻatlarini raqamli formatga oʻtkazish muammolarini, lugʻat maʼlumotlarini toʻplash va tizimlashtirish jarayonini hamda mavjud dasturiy yechimlar tahlilini oʻz ichiga oladi.

**III bob** — "Xorazm shevasidan adabiy tilga tarjimon dasturini loyihalash va yaratish" — lugʻat ma'lumotlarini tozalash, foydalanuvchi interfeysini loyihalash va tarjima mexanizmini Python tilida amalga oshirish masalalariga bagʻishlangan.

**IV bob** — "Hayot faoliyati xavfsizligi" — kompyuter bilan ishlovchi mutaxassislar uchun gipodinamiya, monotoniya va ish joyi mikroiqlimi masalalarini koʻrib chiqadi.

Ishning umumiy hajmi __ sahifani tashkil etadi, foydalanilgan adabiyotlar roʻyxati __ ta manbadan iborat, ilovalarda dasturiy kodning asosiy qismlari va ekran tasvirlari keltirilgan.