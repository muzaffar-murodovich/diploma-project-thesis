# ILOVALAR

## 1-ILOVA. Lug'at namunasi (output_clean.csv fayli ko'rinishi)

Quyidagi jadvalda yaratilgan birlashtirilgan lug'at fayli (`output_clean.csv`) tarkibidan ayrim namunaviy yozuvlar keltirilgan. Yakuniy lug'at 3486 ta yozuvni o'z ichiga oladi.

| sheva       | adabiy                            |
| ----------- | --------------------------------- |
| äldin       | oldin                             |
| ällî        | ellik                             |
| äkä         | aka, ota                          |
| äyqaş-uyqaş | tartibsiz, chuvalashgan           |
| dîlânmaq    | yig'lamoq                         |
| dūzüvlı     | tuzuk, ishlay oladigan            |
| sırt berdi  | yuz o'girdi                       |
| do'ddi      | beso'naqay                        |
| doldirmaq   | to'ldirmoq                        |
| dolîşmaq    | yetilmoq, husnga kirmoq           |
| do:n        | to'n, chopon                      |
| ādik        | etik                              |
| ādiyal      | ko'rpa                            |
| ānqav       | esi past kishi                    |
| bazār       | bozor                             |
| käl         | kel                               |
| tämir       | temir                             |
| yip         | ip                                |
| yilan       | ilon                              |
| gal         | kel                               |

---

## 2-ILOVA. Translit jadvali (kirill ↔ lotin transliteratsiya)

Lug'atning bir qismi kirill yozuvida edi (xususan, "Xorazmcha" mobil ilovasidan olingan ma'lumotlar). `translator.py` da qo'llanilgan kirill-lotin transliteratsiya jadvali:

| Kirill | Lotin | Kirill | Lotin |
| ------ | ----- | ------ | ----- |
| А а    | A a   | Р р    | R r   |
| Б б    | B b   | С с    | S s   |
| В в    | V v   | Т т    | T t   |
| Г г    | G g   | У у    | U u   |
| Д д    | D d   | Ф ф    | F f   |
| Е е    | E e   | Х х    | X x   |
| Ё ё    | Yo yo | Ц ц    | Ts ts |
| Ж ж    | J j   | Ч ч    | Ch ch |
| З з    | Z z   | Ш ш    | Sh sh |
| И и    | I i   | Ъ ъ    | (—)   |
| Й й    | Y y   | Э э    | E e   |
| К к    | K k   | Ю ю    | Yu yu |
| Л л    | L l   | Я я    | Ya ya |
| М м    | M m   | Ў ў    | Oʻ oʻ |
| Н н    | N n   | Қ қ    | Q q   |
| О о    | O o   | Ғ ғ    | Gʻ gʻ |
| П п    | P p   | Ҳ ҳ    | H h   |

---

## 3-ILOVA. Fe'l ildizlari xaritasi (VERB_ROOT_MAP) namunasi

`translator.py` faylida saqlangan sheva fe'l ildizlari va ularning adabiy o'zbek tilidagi muqobillari. Quyida jami 82 ta yozuvdan namunaviy qismi keltirilgan:

| Sheva ildizi | Adabiy ildizi | Misol (sheva)  | Misol (adabiy) |
| ------------ | ------------- | -------------- | -------------- |
| gal          | kel           | galaman        | kelmoqman      |
| gat          | ket           | gataman        | ketmoqman      |
| bar          | bor           | barmaq         | bormoq         |
| ayr          | ayir          | ayirmaq        | ayirmoq        |
| arala        | yarash        | aralamaq       | yarashtirmoq   |
| art          | tozala        | aritmoq        | tozalamoq      |
| dad          | tati          | dadimaq        | tatimoq        |
| dog          | tug'          | dogmaq         | tug'moq        |
| doq          | sovqot        | doqmaq         | sovqotmoq      |
| dun          | tin           | dunmaq         | tinmoq         |
| dura         | urchi         | duramaq        | urchimoq       |
| dushiq       | duch kel      | dushiqmaq      | duch kelmoq    |
| dön          | ayni          | dönmak         | aynimoq        |
| döröt        | yarat         | dörötmak       | yaratmoq       |
| döv          | tuy           | dövmak         | tuymoq         |
| gül          | kul           | gülisha        | kulishmoq      |
| göy          | kuy           | göymak         | kuymoq         |

---

## 4-ILOVA. Fe'l qo'shimchalari xaritasi (VERB_SUFFIX_MAP)

Sheva fe'l qo'shimchalari va ularning adabiy tildagi muqobillari. Jami 30 ta qo'shimcha juftligi:

| Sheva suffiksi | Adabiy suffiksi | Ma'no                |
| -------------- | --------------- | -------------------- |
| -moqdalar      | -moqdalar       | hozirgi z., ko'plik  |
| -avdir / -adir | -yotir          | davomiylik           |
| -aman          | -moqman         | hozirgi z., 1-shaxs  |
| -asan          | -moqsan         | hozirgi z., 2-shaxs  |
| -amiz          | -moqmiz         | hozirgi z., 1-koʻp.  |
| -asiz          | -moqsiz         | hozirgi z., 2-koʻp.  |
| -alar          | -moqdalar       | hozirgi z., 3-koʻp.  |
| -adi           | -moqda          | hozirgi z., 3-shaxs  |
| -dim           | -dim            | o'tgan z., 1-shaxs   |
| -ding          | -ding           | o'tgan z., 2-shaxs   |
| -di            | -di             | o'tgan z., 3-shaxs   |
| -g'in / -gin   | -gin            | buyruq mayli         |
| -sang          | -sang           | shart mayli          |
| -sa            | -sa             | shart mayli          |
| -g'an / -gan   | -gan            | sifatdosh            |
| -magan         | -magan          | inkor sifatdosh      |
| -may           | -may            | ravishdosh           |
| -ib            | -ib             | ravishdosh           |
| -ma            | -ma             | inkor                |
| -maq / -mak    | -moq            | infinitiv            |

---

## 5-ILOVA. Tarjima namunalari (tizim sinovi natijalari)

Quyida ilova tomonidan amalga oshirilgan tarjima namunalari keltirilgan:

**5.1. Alohida so'zlar (2-bosqich — to'g'ridan-to'g'ri moslik):**

| Kiritilgan (sheva) | Natija (adabiy)         |
| ------------------ | ----------------------- |
| äldin              | oldin                   |
| ällî               | ellik                   |
| äkä                | aka                     |
| bazār              | bozor                   |
| ādik               | etik                    |

**5.2. Fe'l shakllari (3-bosqich — morfologik tahlil):**

| Kiritilgan (sheva) | Natija (adabiy) | Tahlil                |
| ------------------ | --------------- | --------------------- |
| galaman            | kelmoqman       | gal + aman            |
| gataman            | ketmoqman       | gat + aman            |
| barmaq             | bormoq          | bar + maq             |
| dîlânmaqda         | yig'lamoqda     | dîlân + maqda         |
| dögmak             | tuymoq          | dög + mak             |

**5.3. Ko'p so'zli iboralar (1-bosqich):**

| Kiritilgan (sheva) | Natija (adabiy)           |
| ------------------ | ------------------------- |
| sırt berdi         | yuz o'girdi               |
| äyqaş-uyqaş        | tartibsiz, chuvalashgan   |
| duch kelmoq        | duch kelmoq               |

**5.4. Gap darajasidagi tarjima:**

- **Kirish:** *Aldin sän dim arriq äduj, indi doliṣib xüṣṣi qiz bolībsan.*
- **Chiqish:** *Oldin sen juda oriq eding, endi yetilib xuddi qiz bo'libsan.*

---

## 6-ILOVA. Loyiha fayllarining tuzilishi

Tarjimon dasturining manba kodi quyidagi tuzilmada joylashtirilgan:

```
xorazmcha.muzaffar/
├── app.py                  — Flask ilovasining asosiy fayli
├── translator.py           — Tarjima mantig'i va lug'at yuklash
├── wsgi.py                 — Gunicorn uchun kirish nuqtasi
├── requirements.txt        — Python kutubxonalari ro'yxati
├── templates/
│   └── index.html          — Asosiy Jinja2 shabloni
├── static/
│   ├── script.js           — Frontend JavaScript (Fetch API, tugmalar)
│   └── style.css           — Responsiv CSS (mobil breakpoint 640px)
├── data/
│   ├── output_clean.csv    — Birlashtirilgan lug'at (3486 yozuv)
│   ├── ocr_natija.txt      — OCR natijalari
│   ├── csv_clean.py        — Lug'atni tozalash skripti
│   └── merge_dicts.py      — Manbalarni birlashtirish skripti
├── deploy/
│   ├── deploy.sh           — Server o'rnatish skripti
│   └── *.service           — systemd va Nginx konfiguratsiyalari
└── .github/
    └── workflows/
        └── deploy.yml      — GitHub CI/CD avtomatik deploy
```

---

## 7-ILOVA. `app.py` — Flask ilovasining manba kodi

```python
from flask import Flask, render_template, request, jsonify
from translator import translate, single_dict, phrase_dict, DICT_SIZE

app = Flask(__name__)


@app.route("/")
def index():
    return render_template("index.html", dict_size=DICT_SIZE)


@app.route("/api/translate", methods=["POST"])
def api_translate():
    data = request.get_json(silent=True) or {}
    text = data.get("text", "").strip()

    if not text:
        return jsonify({
            "translated": "",
            "translated_count": 0,
            "total_words": 0
        })

    translated, translated_count, total_words = translate(
        text, single_dict, phrase_dict
    )

    return jsonify({
        "translated": translated,
        "translated_count": translated_count,
        "total_words": total_words,
    })


if __name__ == "__main__":
    app.run(debug=True)
```

---

## 8-ILOVA. `translator.py` — Tarjima funksiyasining asosiy qismi

```python
def translate(text, single_dict, phrase_dict):
    """
    Matnni tarjima qiladi (besh bosqichli algoritm).
    Qaytaradi: (tarjima, tarjima_qilingan_soni, jami_so'zlar)
    """
    tokens = tokenize(text)
    result = []
    translated_count = 0
    total_words = 0
    i = 0

    while i < len(tokens):
        token = tokens[i]

        if not token.strip() or not re.search(r"\w", token):
            result.append(token)
            i += 1
            continue

        total_words += 1
        token_lower = token.lower()

        # 1-bosqich: Ko'p so'zli iboralarni qidirish
        found_phrase = False
        for phrase_len in (3, 2):
            end_idx = i + phrase_len * 2 - 1
            if end_idx <= len(tokens):
                phrase_words = [t for t in tokens[i:end_idx]
                                if re.search(r"\w", t)]
                if len(phrase_words) == phrase_len:
                    phrase_key = " ".join(w.lower() for w in phrase_words)
                    if phrase_key in phrase_dict:
                        result.append(_match_case(
                            phrase_words[0], phrase_dict[phrase_key]))
                        translated_count += 1
                        i += phrase_len * 2 - 1
                        found_phrase = True
                        break
        if found_phrase:
            continue

        # 2-bosqich: To'g'ridan-to'g'ri moslik
        if token_lower in single_dict:
            result.append(_match_case(token, single_dict[token_lower]))
            translated_count += 1
            i += 1
            continue

        # 3-bosqich: Fe'l morfologik tahlili
        verb_translation = translate_verb(token_lower)
        if verb_translation:
            result.append(_match_case(token, verb_translation))
            translated_count += 1
            i += 1
            continue

        # 4-bosqich: Nom suffiksini ajratish
        suffix_found = False
        for root, suffix in _strip_suffix(token):
            if root in single_dict:
                result.append(_match_case(token, single_dict[root]) + suffix)
                translated_count += 1
                suffix_found = True
                break
            verb_root_trans = VERB_ROOT_MAP.get(root)
            if verb_root_trans:
                result.append(_match_case(token, verb_root_trans) + suffix)
                translated_count += 1
                suffix_found = True
                break
        if suffix_found:
            i += 1
            continue

        # 5-bosqich: O'zgartirilmay qoldirish
        result.append(token)
        i += 1

    return "".join(result), translated_count, total_words
```

---

## 9-ILOVA. `index.html` — Foydalanuvchi interfeysi shabloni

```html
<!DOCTYPE html>
<html lang="uz">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Xorazm shevasi tarjimoni</title>
  <link rel="stylesheet" href="/static/style.css" />
</head>
<body>
  <header class="header">
    <div class="logo">
      <span class="logo-text">Xorazm shevasi tarjimoni</span>
    </div>
    <div class="dict-badge">Lugʻat: {{ dict_size }} ta soʻz</div>
  </header>

  <main class="main">
    <div class="translator-card">
      <div class="lang-bar">
        <div class="lang-label">
          <span class="lang-dot dot-source"></span>
          Xorazm shevasi
        </div>
        <div class="lang-arrow">→</div>
        <div class="lang-label">
          <span class="lang-dot dot-target"></span>
          Oʻzbek adabiy tili
        </div>
      </div>

      <div class="panels">
        <div class="panel panel-source">
          <textarea
            id="source-text"
            class="text-area"
            placeholder="Xorazm shevasida matn kiriting..."
            autofocus
            spellcheck="false"
          ></textarea>
          <div class="panel-footer">
            <span id="char-count" class="char-count">0 belgi</span>
            <button id="clear-btn" class="btn btn-ghost">✕ Tozalash</button>
          </div>
        </div>

        <div class="panel panel-target">
          <div id="target-text" class="text-area text-area-output"
               aria-live="polite"></div>
          <div class="panel-footer">
            <span id="stats-text" class="stats-text"></span>
            <button id="copy-btn" class="btn btn-ghost" disabled>
              📋 Nusxalash
            </button>
          </div>
        </div>
      </div>
    </div>
  </main>

  <script src="/static/script.js"></script>
</body>
</html>
```

---

## 10-ILOVA. Tizim arxitekturasi sxemasi

Veb-ilova quyidagi zanjir orqali ishlab chiqarish muhitida joylashtirilgan:

```
┌──────────────┐
│ Foydalanuvchi│
│   brauzeri   │
└──────┬───────┘
       │ HTTPS
       ▼
┌──────────────┐
│  Cloudflare  │  ← DNS, DDoS himoyasi, SSL/TLS sertifikat
└──────┬───────┘
       │
       ▼
┌──────────────┐
│    Nginx     │  ← Teskari proksi, statik fayllar, yuk taqsimlash
└──────┬───────┘
       │ proxy_pass
       ▼
┌──────────────┐
│   Gunicorn   │  ← WSGI server, ishchi jarayonlar (workers)
└──────┬───────┘
       │ WSGI
       ▼
┌──────────────┐
│ Flask ilovasi│  ← app.py + translator.py
│  (Python 3)  │
└──────┬───────┘
       │ ichki yuklash
       ▼
┌──────────────┐
│ output_clean │
│    .csv      │  ← Lug'at (3486 yozuv)
└──────────────┘
```

**Server muhiti:**
- **Provayder:** Hetzner Cloud
- **OS:** Ubuntu 24.04 LTS
- **Python versiyasi:** 3.x
- **Process manager:** systemd
- **CI/CD:** GitHub Actions (deploy.yml)

---

## 11-ILOVA. Ekran tasvirlari

*(Ushbu ilovaga quyidagi ekran tasvirlarini joylash tavsiya etiladi: 1) bosh sahifa, 2) tarjima jarayoni misoli, 3) mobil ko'rinish, 4) lug'at hajmi badge'i, 5) tarjima statistikasi.)*