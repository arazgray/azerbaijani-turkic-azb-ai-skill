---
name: south-azerbaijani-arabic-script
description: Write and normalize South Azerbaijani Turkic (azb, گۆنئی آذربایجان تۆرکجه‌سی, تۆرکجه) with the rules of "2001 Arabic-script Turk alphabet seminar in Tehran by Dr. Javad Heyat" with exact Unicode vowels, Arabic-loan letter preservation, Iı/İi distinction, hamza, ZWNJ and suffix rules. Use when the user asks for azb, South Azerbaijani, Güney Azərbaycan Türkcəsi, Arabic-script Azerbaijani, transliteration into تۆرکجه, or pastes RTL Azerbaijani text.
license: MIT
metadata:
  language-en: South Azerbaijani Turkic
  language-en-script: South Azerbaijani Turkic (with Arabic Script)
  language-north-en: North Azerbaijani Turkic
  language-north-en-script: Azerbaijani Turkic (with Latin Script)
  language-fa: ترکی آذربایجانی (جنوبی)
  language-fa-script: ترکی آذربایجانی (با الفبای عربی)
  language-north-fa: ترکی آذربایجانی (شمالی)
  language-north-fa-script: ترکی آذربایجانی (با الفبای لاتین)
  language-az-latın: Güney Azərbaycan Türkcəsi
  language-az-latın-script: Ərəb-Köklü Azərbaycan Türkcəsi
  language-north-az-latn: Quzey Azərbaycan Türkcəsi
  language-north-az-latn-script: Latın-Köklü Azərbaycan Türkcəsi
  language-az-arab: گۆنئی آذربایجان تۆرکجه‌سی
  language-az-arab-script: عرب-کؤکلۆ آذربایجان تۆرکجه‌سی
  language-north-az-arab: قۇزئی آذربایجان تۆرکجه‌سی
  language-north-az-arab-script: لاتؽن-کؤکلۆ آذربایجان تۆرکجه‌سی
  short-name: تۆرکجه
  bcp47-parent: az
  bcp47-exact: azb
  bcp47-north-exact: azj
  direction: rtl
  direction-north: ltr
  script: Arab
  standard: Türk Dili Yazı Quralları, First and Second Türk Dili Orthography Seminar, Tehran, final review 5 Oct 2001 (13 Mehr 1380), Dr. Javad Heyat
  authority: 2001 seminar decisions govern spelling. Naming and South-accent policy are extra-manual and labeled as such.
---

# South Azerbaijani Turkic (azb) — Arabic-script orthography

Write `azb` in the 2001 seminar orthography. Do not use Persian, Arabic, Ottoman, North Azerbaijani Latin (`azj`), or Türkiye Turkish spelling habits.

`azb` text is RTL. English, Persian, code, URLs stay in their own direction.

If the user starts in Arabic-script Azerbaijani, treat it as `azb`. Do not ask North vs South.

## 0. Authority and decision order

Word classes (pick one before spelling):

- Native Turkic
- Arabic-origin loan (not nativized)
- Persian-origin loan (not nativized)
- European / other foreign
- nativized loan (only if listed)
- personal name (original vs nativized)
- geographic name
- frozen Arabic phrase

## 1. Alphabet name (seminar §1)

The alphabet name is **تۆرک الیفباسی**. When a contrast is needed, **عرب کؤکلو تۆرک الیفباسی** is also allowed.
The language name is **آذربایجان تۆرکجه‌سی**. When a contrast is needed, **عرب الیفباسیله یازیلان آذربایجان تۆرکجه‌سی** is also allowed.

## 2. Exact glyphs — never substitute

Copy these codepoints. Models routinely emit the wrong lookalikes.

### 2.1 Vowels

| Phoneme | Initial | Else | Codepoints | Examples |
|---|---|---|---|---|
| A a | آ | ا | U+0622 / U+0627 | آتا، آدا، آغیز |
| O o | اوْ | وْ | WAW+SUKUN U+0648 U+0652 | اوْغوز، سوْن، دوْن |
| U u | اۇ | ۇ | U+06C7 | اۇجوز، بۇروق، دۇز |
| Ə ə | ا | ه | U+0627 / U+0647 | ال، دده، ننه |
| E e | ائ | ئ | U+0626 | ائو، گئتمک، یئ، دئ |
| Ö ö | اؤ | ؤ | U+0624 | اؤرنک، گؤن، اؤلکه |
| Ü ü | اۆ | ۆ | U+06C6 | اۆچ، گۆن، دۆنن |
| İ i | ای | ی | U+06CC | ایکی، بیز، دلی |
| I ı | اؽ | ؽ | U+0627+U+063D / U+063D | اؽلدیریم، قؽز، دؽرناق، آیؽ |

**Important distinction for Iı:** `ؽ` is the dedicated letter for the Iı phoneme, but it is **not the normal running-text spelling**. The 2001 manual explicitly says that the Iı diacritic/letter does not normally need to be written and recommends it for teaching materials, foreign words, folklore, or situations where the spelling must be clarified. Therefore, in ordinary prose, do **not** insert `اؽ` / `ؽ` merely because a word contains the Iı sound. Use it only when clarification is actually needed. or user specificly asked to use ؽ/اؽ in any condition. Or a dictionary entry title, which needs to clearify spelling correctly.

A word-initial vowel **must** use the initial carrier. Wrong: ؤلکه، ئل، ئو، ۇجوز. Right: اؤلکه، ائل، ائو، اۇجوز.

Hard substitutions:

- O is `وْ`, not DAMMA. U is `ۇ`, not DAMMA and not bare `و` in the first syllable.
- Ö is `ؤ` (U+0624). Ü is `ۆ` (U+06C6). Never `و` + diaeresis.
- E in native Turkic is `ئ`, never bare `ا` / `ه` / `ع`.
- Iı is `ؽ` (U+063D). Never `ي` U+064A, `ى`, or unmarked `ی` when the phoneme is Iı and contrast with İ matters.
- İ and Y use Farsi Yeh `ی` U+06CC, never Arabic Yeh `ي` U+064A.
- K is `ک` U+06A9, never `ك` U+0643.
- G is `گ` U+06AF. H is `ه` U+0647, never `ھ` or `ە`.
- ZWNJ is U+200C `‌`. It is a letter-level orthographic character.

### 2.2 Vowel-mark modes (seminar §2/3 and §9/6)

The booklet uses dedicated letters in the alphabet table, then allows lighter marking in running text.

Use one mode per text. Default is **standard**.

- **Ordinary running text (default).** Use the booklet's light spelling. Do **not** write `ؽ` / `اؽ` routinely. The 2001 manual says the Iı mark does not need to be written and recommends it specifically for teaching, foreign-word, folklore, or clarification contexts. Thus ordinary prose may use forms such as `آغیز، قاییق، ایشیغیدیر`.
- **Iı clarification mode.** Use the dedicated `ؽ` / `اؽ` only when the Iı vs İi distinction would otherwise be unclear, or when explicitly teaching, documenting, dictionary-style spelling, or otherwise clarifying the orthography. Examples: `قؽز`, `دؽرناق`, `اؽلدیریم`.
- **Marked/primer mode.** When the task explicitly calls for teaching/primer/folklore marking, write the relevant vowel marks more fully (`گؤرۆنۆش، اوْغۇز، دۆیۆن`).
- **Do not “correct” user text** that already follows the booklet’s printed running forms (`بو، آغیز، قاییق، ایشیغیدیر`) unless the user asked for normalization.

§۲/۳: `ؽ` is the dedicated Iı letter, not an accent to add mechanically. Do not add `ؽ` merely because the sound is Iı.

§۹/۴: word-initial Turkic Iı can be represented by the dedicated `اؽ` when clarification/marked spelling is required, but **do not force `اؽ` into ordinary prose**. Exceptions that are actually İ remain `ای`, such as `ایراق، ایلان، اینام`.

### 2.3 Consonants

ب پ ت ج چ خ د ر ز ژ س ش غ ق ف ک گ ل م ن ه و ی

Parenthesized Arabic letters are **only** for Arabic-origin (sometimes Persian-origin) words, never native Turkic:

- ط ث ص ظ ذ ض ح ع
- Native: `سالماق، سوْن، ساققال، ترلان، توْیوق، اوْتاق، ماهنی` (not صالماق، طرلان، ماحنی)

`ع` is kept in Arabic-origin words (`عشق، علم، احسان، مۆعلّیم، مۆعاصیر، منافع`) **and** in frozen Arabic phrases (§13). It is not limited to frozen phrases. Native Turkic still never takes `ع`.

**Arabic-origin spelling preservation:** When a word, personal name, or fixed expression is genuinely Arabic-origin and the manual says its Arabic consonants are preserved, preserve those original Arabic consonant letters. Do **not** replace an Arabic consonant with a phonetically convenient Azerbaijani letter just because the result sounds similar. In particular, Arabic `ع` remains `ع`; never turn it into `ا` or another carrier. Example: `علی` stays `علی`, not `الی`. The same principle applies to other preserved Arabic consonants listed in §3/1. Do not automatically phoneticize an Arabic loan as though it were a native Turkic word.

### 2.4 Auxiliary marks

- FATHA `َ` U+064E — only to disambiguate unwritten Ə (`اَیری، دَیَر، دَوه`)
- KASRA `ِ` U+0650 — only for E in foreign words when confusion is likely (`اِلِمِنت، تِست`)
- SHADDA `ّ` U+0651 — Arabic-origin only
- FATHATAN `ً` U+064B — Arabic tanvin only (`مثلاً`)
- SUKUN `ْ` U+0652 — part of O (`سوْن`)
- HAMZA — §8 only

## 3. Ə (seminar §2.1) — write sparingly

Ə and E are different phonemes. Never convert one into the other.

- Word-initial Ə = `ا` (`ال، اپریمک`). Not `ائ`.
- End of a morpheme or syllable = `ه` (`گؤزله‌مه‌دی، دسته‌له‌مک، وظیفه‌لی، دده‌م`)
- Middle of a morpheme or syllable = omit (`گتیرمک، درین، دلی، گل، گلن، گلنیم`)

Resolution:

1. A morpheme shorter than one syllable merges left: `ایزله‌مک` → `ایزلنمک`, `ایشله‌مک` → `ایشلتمک`.
2. Exception: a short possessive still counts as its own morpheme: `دده‌م، اؤنرگه‌ن، وظیفه‌م`.
3. Ə at the end of the **first** syllable is omitted: `گتیرمک، درین، دلی`.
4. A one-syllable word ending in Ə writes it: `نه، ده`.
5. Keep root and suffix spelling stable: `گل / گلن / گلنیم` (not `گله‌نیم`).
6. If morphemes cannot be cut cleanly, spell by syllable: `گؤبه‌لک، چییه‌لک، کپه‌نک، یئلپه‌نک، کؤنده‌لن، کلبه‌جر، چته‌نه، گؤره‌لیم، گؤزله‌یه‌لیم، بیله‌رک، گله‌نک`.
7. If omission is ambiguous, add FATHA: `اَیری، دَیَر، دَوه`.

Both morpheme and syllable accounts yield the same written form:

`چؤرک→چؤرگیم`، `گلن→گلنی`، `گؤزل→گؤزلیم`، `گۆلش→گۆلشه‌جک`، `تبریز→تبریزدنم`، `گلسه→گلسه‌یدی`، `گلمک→گله‌جک / گلجک / گله‌لی` (three different words; keep them distinct).

Wrong: `ده‌لی، گه‌لمه‌ک، گؤزه‌ل، چؤره‌ک، تبریزده‌نم، گؤره‌نیم`.

## 4. E (seminar §2.2)

- Native Turkic: always write `ئ` / `ائ`. `ائشیدیرم، دئمه‌میشم، گئدیرم، گئجه، دئدیم، یئ، دئ`. Never `گجه، ددیم`.
- Loans, initial/medial: normally omit E. `انرژی، الکتریک، تلویزیون، تکنولوژی، احسان، علم، حکایه، فاتح، عشق`. Optional KASRA if needed: `اِلِمِنت، تِست`.
- **Closed exception — next to Y, always write E**, native or loan: `قئید، مئیل، سئیر، شئیدا، گۆنئی، سئیرک، حئیرت، غئیرت، جئیران، تقی‌یئف، یئکۇن، ویئتنام، هئیأت`. Never `میل، قید، شی`.
- Original İ, local E, also write E: `تسبئح، قبئح، سفئه، بئچارا، بئساواد، پئشواز، پئشکش`.
- Do not invent E: `مهربان` not `مئهربان`.

## 5. Consonant rules (closed environments only)

1. V = bare `و`. Keep the documented double-waw after Ö: `دؤولت، شؤوکت، دؤوران` (not `دؤلت`).
2. H = bare `ه`: `همیشه، ساهمان، مئه، شئه، آللاه، هله`. Native Turkic never `ح`.
3. Y = bare `ی`: `یایلیق، بایرام، آی`.
4. **Yumşaq g — closed class, seminar §3/5 only.** Y *between two İ* in this set is written `گ`: `ایگید، ایگیرمی، چیگین، گتیردیگیم`. Do **not** apply to `اییده، گؤیرچین، گؤی، دییرمان، دئییل، دییشمک` (those stay with `ی`). Wrong: `ایگده، گؤگرچین، گؤک، دگیرمان، دگیل، دگیشمک`.
5. Intervocalic `ک` that has become a Y-sound is written `گ` to keep the root visible: `چؤرگیم، گله‌جگیم، گله‌جگم، گؤروندوگو، الجگیم، شاعیرلر درنگی`. Not `چؤره‌ییم، گله‌جَیَم، گؤروندویو`.
6. Thick European K = `ک` not `ق`: `دوْکتور، دموْکراسی، کاراکتر`.
7. Final Arabic `ع` pronounced H = `ح`: `ماتاح، طاماح`. Medial = `ه`: `فهله`.
8. Foreign `غ` pronounced Q is still `غ`: `غریب، غزل، غم، افغان، غۇصّه`.
9. Persian `گ` pronounced Q is still `گ`: `کارگاه، آگاهی، دانیشگاه، آبگوشت، گۇماشتا`.

## 6. Clusters and foreign words

- Foreign İA / İO / İU: one `ی` only. `رادیوْ، بیوْلوژی، کیوْسک، دیالکتیک، نیویوْرک، خیاوان، ریاضی، سیاست`. Never `خییاوان، رییاضی`.
- Initial SP ST ŞP ŞT SK only: prepend `ای`. `ایسپورت، ایستالین، ایستانسیا، ایستراسبورق، ایستئیک، ایسکنر، ایشتوتقارت، ایشنیتسل`.
- Do **not** prepend `ای` to other foreign clusters. Unsettled in the seminar: `پلان، پروگرام، کرونولوژی`, and `واو معدوله`. Leave those as commonly written or flag them.
- European loans follow French reading: `رداکسیوْن، ناسیونال، انرژی`.
- Latin G that is Q in Latin Azerbaijani = `ق`: `اوْرتوقرافی، قرامر، قاز`.
- European ae = `آی`: `آیروپورت، آیروپلان`.
- Otherwise phoneticize with Turkic vowels: `مۆشکول، ایستیقلال، اینسان، مۆعاصیر، مۆعلّیم، ظالیم، صؤحبت، ورزیش، تلویزیون`. Not `مشکل، استقلال، ورزش`.
- Nativized loans are a list, not a converter. Listed: `مۇغایات، هامبال، باریت، مؽزی، آبیر، آمبار، قایدا، طایفا، فایدا`. Unlisted Arabic/Persian loans follow ordinary loan rules.

More examples: `references/examples.md`.

## 7. Tashdid and tanvin

Tashdid only in Arabic-origin words: `مۆکمّل، ادبیّات، موفّقیّت، مدنیّت، عمّه، عطّار، حیصّه، حاقّیندا`.

Turkic doubles the letter: `چاققال، ائششک، دوْققوز`. European: `اوْتللوْ`. Never shadda there.

İYY / İY in loans: one `ی`, shadda only if needed. `مدنیّت، ادبیّات، سویّه، قیمت، صحیّه، ویئتنام، کیئف`. Never `صحییّه، سوییّه`.

Tanvin only where Arabic requires it: `مثلاً، اعتیباراً، قصداً، سهواً، قطعیاً، عملاً`. Never `مثلن`. Hamza+tanvin: `جۆزئاً، ایستیثنائاً`.

## 8. Hamza

| Environment | Form | Examples |
|---|---|---|
| Word-final silent hamza after Ə | أ | منشأ، مبدأ، ملجأ |
| After U | ء | سۇء |
| After A, silent in speech | omit | اینشا، ایملا، ایجرا، انبیا، اؤولیا |
| Voiced with A | آ (madda only if needed) | سۇال، مۇاخیذه، مبدآت، اینشاآت، مآل |
| Voiced with Ə | أ | جۆرأت، تأسّوف، هئیأت، مسأله، نشأت |
| That Ə is word-final | ئ | نشئه، تؤوطیئه |
| Voiced with İ | ی | رییس، فدایی، جرایید، ایسراییل، کایینات، داییر |
| Voiced with O / U / E | ئ | ناپلئون، زئۇس، دۇئل، سۇئد، مائوْ، مسئۇل، ایدئوْلوژی |
| After E | ئ | تئاتر، رئال، نئاندرتال، پروتئین (also پروتیین) |
| After Ö / Ü | omit | مؤمین، لؤلؤ، مۆدّب، مۆلّیف، مۆثّیر |
| Possessive on منشأ / مبدأ | keep أ + یی | منشأیی، مبدأیی |

`هئیأت` is the common noun. The personal name in §12 may stay `هیئت`.

## 9. Suffixes — MUST attach vs MUST ZWNJ vs MAY ZWNJ

ZWNJ = `‌` U+200C. Never replace a prescribed ZWNJ with a space. Never insert ZWNJ where the booklet attaches.

**MUST attach (no ZWNJ, no space):** ordinary suffixes. `گلمیشم، گلدیلر، ائللر، گؤزلدیر، اینسانلار، گۆنشلر`.

**MUST distinguish `دا/ده` by function:**

- suffix → attach: `منده‌دیر`
- independent word “also” → space: `حسن ده گلدی، من ده`

**MUST write `می/مو` as juxtaposition, never space:**

- middle of the word: ZWNJ. `گلدی‌می؟ گئتدی‌می؟`
- at the end: side-by-side with ZWNJ, not a space. `نه‌سن؟` not `نه سن`. Poetry line keeps that pattern (`نشترمیسن، نه‌سن؟`).

**MUST ZWNJ before suffixes that begin with a linking consonant** (seminar §8/4 examples): `نین/نؽن، یه/یا، ییک/یؽق، ییر/یؽر، یئف، یئوا`.

`موسیقی‌سی، قالمالی‌یام، قالمالی‌ییق، دئمه‌لی‌یم، دئمه‌لی‌ییک، فیضولی‌یه، ننه‌نین، تملی‌نین، علی‌یه، ماهنی‌یا، قالمالی‌یؽق، لنگی‌ییر، تقی‌یئف، تقی‌یئوا، تانری‌نین، تانری‌یا، یئری‌ییر`.

Wrong: `تانرینین، تانرییا، دئمه‌لیییک، یئریییر، تقییئف`.

**MAY ZWNJ**

- 4+ syllables, after a vowel-final morpheme, no space: `مۇسیقی‌چیلر، بیزیمکی‌لر`
- same/similar consonant three times in a row: `سس‌سیز`
- same/similar letter at a morpheme joint and the first letter joins from the right: `نسیل‌لر، منیم‌میش، دیل‌لنمک`
- if that consonant does **not** join from the right, attach left: `اللر، داممیش، آشسیز، گؤللنمک`

**MUST attach — borrowed formatives group (a):** کار، خانا، دار، گاه، کده، بئ، پاز، باز، بر، جو، ایزم، پئش، کش، گر، زده، خواه، نامه، زن، خوْر، دان، یستان، زادا، سن، هم، اوْف، اوْوا.

`صنعتکار، کیتابخانا، محصولدار، دانیشگاه، دانیشکده، بئکار، آشپاز، قۇشباز، دیلبر، سیمینبر، دانیشجو، صۆلحجو، متابوْلیزم، پئشواز، قایغیکش، میسگر، غربزده، ترقیخواه، شیکایتنامه، لافزن، رۆشوتخور، نمکدان، دشتیستان، ملیکزادا، سنتز، همصؤحبت، حسنوف، حسنوْوا`.

**MUST ZWNJ — borrowed formatives group (b):** شۆناس، پرست، طلب، فۆرۇش، آنتی، پرور، پان.

`آذربایجان‌شۆناس، وطن‌پرست، شؤهرت‌طلب، فضل‌فۆروش، آنتی‌کوْمونیست، قوْناق‌پرور، پان‌عربیزم`.

## 10. Compounds and phrases

- Native compounds: parts independent, juxtaposed with ZWNJ, no space, no full fusion of the short type. `آغ‌ساققال، آغ‌بیرچک، ککلیک‌اوْتو، ایت‌بۇرنو، دیک‌باشلیق`.
- Do not force ZWNJ into booklet solids: `قانۇنااۇیغونلوق، گؤزوگؤتورمزلیک`.
- Foreign compounds: same treatment as compounds, ZWNJ. `مؤهنت‌افزا، دیل‌آرام، وطن‌پرست، شؤهرت‌طلب`.
- Persian constructs where at least one part has standalone meaning: hyphen. `سیمای-شمس، زۆلف-پریشان، سۇء-قصد، باده‌ی-ناب، غیر-مۆمکون، ضیدّ-اینقیلاب`. Otherwise one lexical unit.
- Borrowed `و`: as-is or with Ü. `گشت و گۆذار` / `گشت ۆ گۆذار`.
- Frozen Arabic phrases keep original Arabic spelling: `علی‌الخصوص، سهل‌الهضم، میزان‌الحراره، نعوذبالله، استغفرالله، انشاالله، ماشاالله، الی‌آخر`.

## 11. Names, geography, numbers

- Non-nativized Persian/Arabic personal names keep original spelling: `محمّد، حسین، ابوالقاسم، منوچهر، کاظم، عبدالناصر، کبری، ساعد، هیئت`.
- Nativized names are a separate list and *may* use azb spelling: `علسگر، فاطما، حۆسئن، ایرضا، ممّد`. Do not auto-convert every name.
- Geography as used in Iran, adapted where possible: `لهیستان، اؤزبکیستان، هیندوستان، لۆبنان، اوْتریش، تۆرکیه، کۆردوستان`.
- Distorted place names: restore when possible. `تۇفارقان، سئییدآوا، سایین قالا، سۇلدوز، آخما قایا`.
- Turkic words used in Persian: azb spelling. `بوْشقاب، اۆتو، شۇلوق، اۇمود، قۇلدور`.

Numbers: digit + hyphen + suffix. Do not invent extra number spellings.

| Function | Forms |
|---|---|
| Ordinal | ۲-جی، ۳-جو، ۶-جی، ۹-جو، ۱۳۷۹-جو ایل |
| Accusative | ۱۱-ی، ۱۲-نی، ۱۳-ۆ، ۶-نی |
| Locative | ۱۱-ده، ۱۲-ده، ۶-دا، ۹-دا |
| Dative | ۱۱-ه، ۱۲-یه، ۶-یا، ۹-ا |
| Ablative | ۱۱-دن، ۱۲-دن، ۶-دان، ۹-دان |
| Genitive | ۱۱-ین، ۱۲-نین، ۴-ۆن، ۵-ین |
| Possessive | ۱۱-ی، ۱۲-سی، ۹-و، ۷-سی |

`ساعات ۱۱-ده`، `۱۲-یه خبر وئرین`، `خۇردادین ۷-سی`.

## 12. Unsettled — do not invent

- `واو معدوله` (deferred by the seminar)
- foreign initial clusters outside SP ST ŞP ŞT SK, including `پلان، پروگرام، کرونولوژی`
- unlisted nativized loans (promised to an orthography dictionary)
- abbreviations (`قیسالتمالار` was a seminar topic, not a published rule set)

If asked to settle one of these, state that the 2001 decisions left it open.

## 12.5 Two critical anti-errors

### A. Arabic-origin letters must not be silently replaced

For Arabic-origin loans, Arabic personal names, and frozen Arabic expressions, first determine whether the manual requires preservation of the original Arabic consonant spelling. If yes, preserve it.

- `علی` → `علی`, **not** `الی`
- `عشق` → `عشق`, **not** a form that removes `ع`
- `علم` → `علم`, **not** a form that replaces `ع`

Do not confuse phonetic pronunciation with orthographic replacement. The South Azerbaijani system adapts many loanwords, but it does not authorize arbitrary replacement of preserved Arabic consonants.

### B. `I ı` is not the same as `İ i`

There are two separate issues:

- `İ i` uses `ی` U+06CC.
- `I ı` has the dedicated letter `ؽ` U+063D, with initial `اؽ`.

However, **ordinary prose should normally not mark Iı with `ؽ`**. The manual says the Iı mark does not need to be written and recommends it when differentiation is needed, especially for teaching, foreign-word, folklore, dictionary, or spelling-clarification contexts.

Therefore:

- Do not mechanically convert every Iı sound to `ؽ`.
- Do not use `ؽ` as a general replacement for `ی`.
- Do not use `اؽ` at the beginning of every word containing Iı.
- Use `ؽ` / `اؽ` when the distinction from `İ` matters or when the text is explicitly marked for teaching/clarification.
- Never confuse the dedicated Iı letter `ؽ` with Arabic Yeh `ي` or Farsi Yeh `ی`.

## 13. Pre-output checklist

1. Class the word. Apply only that class’s rules.
2. Cut morphemes and syllables **before** spelling Ə.
3. Word-initial vowel uses the carrier form.
4. Glyphs: `وْ ۇ ؤ ۆ ئ ؽ ی ک`. `ؽ` is a marked/clarifying Iı form, not a default running-text vowel. Scan for wrong lookalikes such as `ي`, `ك`, and unintended `ؽ` overuse.
5. E next to Y is written. Ə is not written as `ئ`.
6. Yumşaq g and intervocalic `ک→گ` only in the environments in §5.
7. `ع ح ط ض ظ ذ ث ص` only in the right loan class, but do not strip `ع` from Arabic loans.
8. Hamza / tashdid / tanvin from §7–§8 only.
9. Suffixes: attach vs ZWNJ vs space by §9. `می/مو` never uses a space.
10. Do not analogize unlisted nativized words.
11. Policy §16 only when generating free South prose, not when normalizing a supplied spelling.
12. If the booklet has no rule, do not fabricate one.

## 14. Minimal targets

`یار بیزه قوْناق گله‌جک.` (future; not participle `گلجک`)

`حالال چؤرگیم بۇ سۆفره‌نین ایشؽغؽدؽر.`

`هر گلنی قارداش تانیمازلار.`

`آتام بۇ آخشام تبریزدن گله‌جک.`

`عاراقچینین منده‌دیر.` / `حسن ده گلدی، من ده.`

`تانری‌نین آدییلا.` / `تانری‌یا یالوارماق.`

`هئیأت، جۆرأت، مسأله، رییس، اینشا، منشأ`

`اینسانلار` not `اینسان‌لار`. `آذربایجان‌شۆناس` not `آذربایجانشۆناس`.

`بیزیمکی‌لر مۇسیقی‌چیلرله گؤروشدو.`

## 15. Hard failures

| Wrong | Right |
|---|---|
| قیز | In marked/clarification mode: `قؽز`; in ordinary running text, do not force `ؽ` unless the distinction is needed. |
| سون، اوغوز | سوْن، اوْغوز |
| بوروق، ترک | بۇروق، تۆرک |
| ئل، ئو، ؤلکه، ۇجوز | ائل، ائو، اؤلکه، اۇجوز |
| میل، شی | مئیل، شئی |
| چؤره‌ییم، دگیل | چؤرگیم، دئییل |
| ایگده | اییده |
| چاقّال، دوْقّوز | چاققال، دوْققوز |
| مشکل، استقلال، ورزش | مۆشکول، ایستیقلال، ورزیش |
| اسپورت، خییاوان | ایسپورت، خیاوان |
| مثلن، منشه، رئیس، اینشاء | مثلاً، منشأ، رییس، اینشا |
| اینسان‌لار، آذربایجانشۆناس | اینسانلار، آذربایجان‌شۆناس |
| ي، ك | ی، ک |
| دؤلت، شؤکت | دؤولت، شؤوکت |
| طاماه | طاماح |
| تانرینین، تانرییا | تانری‌نین، تانری‌یا |
| گلدی می | گلدی‌می |
| الی (for Arabic `علی`) | علی |
| routine `ؽ` marking in ordinary prose | use unmarked running form unless Iı/İ must be clarified |

## 16. Policy — not seminar orthography

Apply only when generating or translating free South prose. Do not apply when the user asked to normalize, quote, or keep a given word.

- Answer in the South (Tabriz) accent. South form wins over North. Documented pair for this policy: `سلام` not `سالام`.
- Do not use Russian-origin or Republic-of-Azerbaijan everyday loans. Use the South equivalent.
- Prefer a common South/Turkic word over a Persian/Arabic loan when it stays natural and clear. Keep the loan when replacement would sound forced. Intelligibility wins.

Language names and codes: `references/naming-policy.md`.
