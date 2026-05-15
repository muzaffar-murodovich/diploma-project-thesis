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

**Birinchi bosqich - manba materiallarini tayyorlash.** "Xorazm shevalari lugʻati" (2024)ning sahifalari skanerdan oʻtkazilgan va OCR texnologiyasi yordamida matn ajratib olingan. Maxsus transkripsiya belgilarini qayta ishlash uchun dastlabki belgilarni normallashtirish (normalizatsiya) funksiyasi ishlab chiqilgan. Masalan, turli variantlarda uchraydigan ø, ö, ü kabi belgilar standart koʻrinishga keltirilgan.

**Ikkinchi bosqich - maʼlumotlarni tozalash va standartlashtirish.** Avtomatik tarzda ajratib olingan lugʻat yozuvlari qoʻlda tekshirilgan. Geografik izohlar (mahalla nomi, qishloq nomi va h.k.) alohida maydonlarga ajratilgan. Raqamli yoki ketma-ket koʻrsatilgan koʻp maʼnoli soʻz izohlari qayta tarkiblashtirilgan.

**Uchinchi bosqich - morfologik tahlil va tarjima mexanizmini yaratish.** Sheva soʻzlarini adabiy oʻzbek tiliga tarjima qilish uchun ildiz soʻz va qoʻshimchalarni ajratuvchi morfologik tahlilchi - lemmizator - ishlab chiqilgan. Feʼl ildizlari va sheva qoʻshimchalari alohida lugʻat jadvallari sifatida saqlanib, tarjima jarayonida ular ketma-ket qoʻllaniladi.

**Toʻrtinchi bosqich - foydalanuvchi interfeysi.** Raqamlashtirilgan lugʻat materiallariga qulay kirish imkonini beruvchi interaktiv tarjimon dasturi yaratilgan. Ushbu dastur soʻz qidirish, morfologik tahlil qilish va sheva matnini adabiy tilga tarjima qilish funksiyalarini oʻz ichiga oladi.
