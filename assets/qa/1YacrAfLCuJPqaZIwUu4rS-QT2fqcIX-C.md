# Raport Dowodowy Niezależnego QA — Stream B2 (Publikacje 4–6 + 11 rozkładówek + `GR-UNKNOWN-P03`)

**Data weryfikacji:** 2026-11-22  
**Rola:** Niezależny Agent QA (Stream B2)  
**Metodologia:**
1. Programowa weryfikacja **100% linków Google Drive i nazw JPG** we wszystkich 4 jednostkach katalogowych (`BOL-ISSUE-UNNUMBERED-995E`, `BOL-ISSUE-OCHOANOS-UNKNOWN`, `PRINT-UNKW-INSTITUTION-04-10`, `GR-UNKNOWN-P03`) przeciwko `/home/antigravity/patronato_final/MASTER_CATALOG_PATRONATO_ALMU_v7.json` (łącznie 20/20 źródłowych JPG) oraz weryfikacja obecności plików w `/home/antigravity/patronato_closure/upright/`.
2. Bezpośrednia, niezależna weryfikacja wizualna przeciwko oryginalnym fotografiom JPG z `/home/antigravity/patronato_closure/upright/`, przetworzonym w PIL (obrót 90° CCW + kontrast dla `GR-UNKNOWN-P03`; obrót 180° + rozdzielenie na pojedyncze strony dla rozkładówek; dodatkowy obrót 90° CW dla tabel apaisados na s. 10–11, 12 i 16–17).
3. Uczciwe nadanie statusów QA:
   - **`INDEPENDENT_QA_PASS_FULL`** wyłącznie dla dokumentu sprawdzonego w 100% słowo po słowie (`GR-UNKNOWN-P03_ATTEMPT_ES.md`),
   - **`BLOCKED_VERIFIED_QA_PASS`** dla publikacji zablokowanej przez filtr API (`PRINT-UNKW-INSTITUTION-04-10_ES.md`),
   - **`QA_SPOT_CHECKED`** dla wielostronicowych biuletynów i zbiorczego pliku 11 rozkładówek.

---

## 1. Tabela werdyktów QA (Stream B2)

| # | Plik w `/home/antigravity/patronato_closure/stream_b/` | Zakres JPG / Strony | Werdykt QA | Podsumowanie ustaleń |
|---|---|---|---|---|
| 1 | `GR-UNKNOWN-P03_ATTEMPT_ES.md` | 1 JPG (`1ZOubqnz0bEvvkijAIIaVDgNCcMlh8f3O.jpg`), 100% słowo po słowie | **`INDEPENDENT_QA_PASS_FULL`** | 1/1 link v7 zgodny. Obrót 90° CCW + kontrast w PIL potwierdzają 100% zgodność słowo po słowie (teczka `AHPTO 15429 Ac 2949/3` + strona `- 3 -` z 2 punktami o komisjach). 0 rozbieżności. |
| 2 | `PRINT-UNKW-INSTITUTION-04-10_ES.md` | 4 JPG (s. 4–10 + wyklejka tylna), zablokowane API | **`BLOCKED_VERIFIED_QA_PASS`** | 4/4 linki v7 zgodne. Struktura nagłówków s. 4–5 i s. 10, prześwit stopki `MINISTERIO DE JUSTICIA / BOLETIN DE INFORMACION` oraz dokumentacja blokady API bez halucynacji i bez obchodzenia filtra w 100% potwierdzone. Dopasowanie do `1251bf71` (s. 2–3) potwierdzone ciągłością sylabową (`califica-` → `do y de muebles...`). |
| 3 | `BOL-ISSUE-UNNUMBERED-995E_ES.md` | 8 JPG (s. 2–3, 6–9, 12–20; brak s. 1, 4–5, 10–11 w tym locie) | **`QA_SPOT_CHECKED`** | 8/8 linków v7 zgodne. *Sumario* s. 2, liczby w *Editorial* s. 3 (`19`, `763`, `247`, `114`, `22`, `23`, `277`, `1.092`, `960`, `3.098`, `284`), cała tabela apaisada s. 12 (wiersz po wierszu, cyfra po cyfrze) i s. 20 — 0 błędów. Dopasowania `cb7fef27` (s. 4–5) i `cd3cd384` (s. 10–11) potwierdzone fizycznie. |
| 4 | `BOL-ISSUE-OCHOANOS-UNKNOWN_ES.md` | 7 JPG (s. 2–3, 6–15, 18–19; brak s. 1, 4–5, 16–17, 20 w tym locie; s. 6–7 zablokowane API) | **`QA_SPOT_CHECKED`** | 7/7 linków v7 zgodne. *Sumario* s. 2, *Editorial* s. 3, rzetelna dokumentacja blokady API na s. 6–7 (*Circular Fiscalía TS*, 3-IV-1963) oraz s. 19 (*Escuela de Reeducadoras*, 28 czerwca, 34 uczennice) — 0 błędów. Dopasowania `df7c4124` (s. 4–5) i `8253f3e3` (s. 16–17) potwierdzone fizycznie (prześwity rewersu!). |
| 5 | `UNASSIGNED_11_SPREADS_AUDIT_AND_ES.md` | 11 rozkładówek `druk` (6 dopasowań + 5 wolnych) | **`QA_SPOT_CHECKED`** | Wszystkie 6 kluczowych odkryć dopasowań (`cb7fef27`, `cd3cd384`, `df7c4124`, `8253f3e3`, `1251bf71`, `dba54c80`) potwierdzone w 100% przeciwko JPG; tabele s. 10–11 i s. 16–17 oraz `65b525af` sprawdzone cyfra po cyfrze (0 błędów w transkrypcji). **Wykryto i naprawiono bezpośrednio 2 błędy metadanych** (krytyczny błąd dot. `BOL-1956-01_ES_Claude.md` oraz zły licznik wierszy `26` → `31` dla `65b525af`). |

---

## 2. Programowa weryfikacja linków JPG (vs `MASTER_CATALOG_PATRONATO_ALMU_v7.json`)

- **`BOL-ISSUE-UNNUMBERED-995E` (cat. 106):** 8/8 `source_jpgs` (nazwa UUID + Google Drive ID) obecne i poprawne w `BOL-ISSUE-UNNUMBERED-995E_ES.md`.
- **`BOL-ISSUE-OCHOANOS-UNKNOWN` (cat. 107):** 7/7 `source_jpgs` (nazwa UUID + Google Drive ID) obecne i poprawne w `BOL-ISSUE-OCHOANOS-UNKNOWN_ES.md`.
- **`PRINT-UNKW-INSTITUTION-04-10` (cat. 108):** 4/4 `source_jpgs` (nazwa UUID + Google Drive ID) obecne i poprawne w `PRINT-UNKW-INSTITUTION-04-10_ES.md`.
- **`GR-UNKNOWN-P03`:** 1/1 `source_jpgs` (`41de391c-4848-4d14-8aab-a0556d5b5639.jpg` / `1ZOubqnz0bEvvkijAIIaVDgNCcMlh8f3O`) obecny i poprawny w `GR-UNKNOWN-P03_ATTEMPT_ES.md`.

---

## 3. Szczegółowe dowody weryfikacji wizualnej

### 3.1. `GR-UNKNOWN-P03_ATTEMPT_ES.md` — **`INDEPENDENT_QA_PASS_FULL`**
- **Źródłowy JPG:** `1ZOubqnz0bEvvkijAIIaVDgNCcMlh8f3O.jpg` (1200×1600), obrócony o 90° CCW + `autocontrast` i kontrast ×2.0 w PIL.
- **Lewa połowa (teczka archiwalna):**
  - Rękopis w prawym górnym rogu: `AHPTO 15429   Ac 2949/3` — **100% zgodne**.
  - Druk z herbem: `Junta de Comunidades de / Castilla-La Mancha / Consejería de Educación y Cultura` — **100% zgodne**.
  - Ramka dolna: `ASUNTOS: Patronato de Protección a la Mujer / circulares` — **100% zgodne**.
- **Prawa połowa (strona maszynopisu `- 3 -`):**
  - `- 3 -`
  - `- Comisión para estudiar qué instituciones son más necesarias y cómo fomentar la creación de las que no existen.`
  - `- Comisión para estudiar el perfeccionamiento de las Celadoras en el curso de su empleo.`
  - Fragment wystającej karty pod spodem z prawej: `BOA, 33` — potwierdza notę archiwistyczną.
- **Werdykt:** 100% zgodności słowo po słowie, znak po znaku → **`INDEPENDENT_QA_PASS_FULL`**.

### 3.2. Kluczowe odkrycia dopasowań w `UNASSIGNED_11_SPREADS_AUDIT_AND_ES.md` — **`QA_SPOT_CHECKED`** (2 błędy metadanych naprawione)
1. **`dba54c80` (`1aGP3PsRzJfZwSETWv3VGIuMUNmEEHj4_`) → `BOL-1956-01`, s. 6–7 (KRYTYCZNE ODKRYCIE I POPRAWKA METADANYCH):**
   - Wizualnie potwierdzono paginację `— 6 —` i `— 7 —`.
   - Strona 6 zaczyna się dokładnie od `mente al Organo competente del Patronato de Protección a la Mujer...`, co jest **bezpośrednią kontynuacją sylabową** urwanego końca s. 5 w `/home/antigravity/patronato_closure/claude/BOL-1956-01_Boletin_Num_1_1956-05-05_ES_Claude.md` (`En tales casos, se dará cuenta inmediata-`).
   - Dalej: pkt `11.` Orden de la Presidencia del Gobierno, `Madrid, 23 de abril de 1956.—Carrero.`, a następnie pełna **`Circular de la Junta Nacional número 47.`** (pkt 1.º–4.º na s. 6; `Internamiento.`, pkt 5.º–6.º, akapity końcowe i odręczna parafa na s. 7; w prześwicie rewersu ceny prenumeraty *Ministerio de Justicia - Sección de Publicaciones*).
   - **WYKRYTY I NAPRAWIONY BŁĄD METADANYCH (linia 456):** Agent B2 błędnie zapisał, że *«transcripción íntegra ya disponible en `/home/antigravity/patronato_closure/claude/BOL-1956-01_Boletin_Num_1_1956-05-05_ES_Claude.md`»*. Sprawdzono plik Claude'a bezpośrednio: ma status **`INCOMPLETE`** i zawiera **wyłącznie strony 1–5** (*«Faltan la p. 6 y siguientes, con el final del punto 10 de la Orden y la «Circular de la Junta Nacional número 47»*»). Oznacza to, że `dba54c80` jest **nowo odnalezioną brakującą rozkładówką zamykającą fizycznie `BOL-1956-01`** (zablokowaną aktualnie przez filtr praw autorskich API do transkrypcji literalnej). Poprawiono bezpośrednio w `UNASSIGNED_11_SPREADS_AUDIT_AND_ES.md`.
2. **`1251bf71` (`1X3OyEbVVTX18uepPFau1klp5AYTSkl25`) → `PRINT-UNKW-INSTITUTION-04-10`, s. 2–3:**
   - Prześwit rewersu s. 2 (po wzmocnieniu kontrastu w PIL): wyraźnie `MINISTERIO DE JUSTICIA / BOLETIN DE INFORMACION / ANEXO DEL PATRONATO DE PROTECCION A LA MUJER / ORGANO OFICIAL DEL DEPARTAMENTO / NUM. 393 / AÑO XI / NUMERO 4 / MADRID`.
   - Strona 3: nagłówek *Extracto del folleto publicado por el Departamento de Asuntos Económicos y Sociales de las Naciones Unidas (Nueva York, 1957), sobre la ASISTENCIA EN LAS INSTITUCIONES*, dwa akapity noty redakcyjnej (100% zgodne), sekcje *Situación de los edificios.* i *Tipo y tamaño de los edificios.*, zakończona wyrazem `lo menos de un personal altamente califica-`, który **łączy się dosłownie** z początkiem s. 4 w `PRINT-UNKW-INSTITUTION-04-10` (`do y de muebles y accesorios de tipo doméstico".`).
3. **`cb7fef27` (`1hfUpP0rtBct1vynW7eqj0Oxr_JyafTxC`) → `BOL-ISSUE-UNNUMBERED-995E`, s. 4–5:**
   - Paginacja `— 4 —` i `— 5 —`. Strona 4 rozpoczyna się od rozbicia 284 przyjęć z s. 3 (`113 + 142 + 27 + 1 + 1 = 284`), wszystkie 16 liczb i dat na s. 4 oraz zakończenie z mottem w ramce na s. 5 — **100% zgodne**.
4. **`cd3cd384` (`1HTgwq09GWzw61KW7pn2EqwVNdmIZVIOg`) → `BOL-ISSUE-UNNUMBERED-995E`, s. 10–11:**
   - Obrócono tabele apaisadas o 90° CW i zweryfikowano **100% wierszy i liczb na s. 10 i s. 11** (`298` przez `364` na s. 10; `308` przez `279` + *Cursillos en tramitación* na s. 11) — **0 błędów**. W prześwicie rewersu s. 11 widoczne `Nuevos cursos (en tramitación)` z s. 12 `995E` (fizyczny dowód ciągłości!).
5. **`df7c4124` (`1j48sKkprDB8h7rRAHaWr4rgwSDadKPPC`) → `BOL-ISSUE-OCHOANOS-UNKNOWN`, s. 4–5:**
   - Paginacja `— 4 —` i `— 5 —`. Zaczyna się od `y conocer «de visu»...` (ciągłość z s. 3 `para establecer contacto con ellas`). Wszystkie 17 nowych placówek od `ALBACETE` do `TENERIFE`, cytat *Marcel Sacotte* i prześwit tytułu `Circular de la Fiscalía del Tribunal Supremo...` z s. 6 `OCHOANOS` — **100% zgodne**.
6. **`8253f3e3` (`1tPOYL2sIKkQswrtAd80_X1O-I6M1WEF7`) → `BOL-ISSUE-OCHOANOS-UNKNOWN`, s. 16–17:**
   - Obrócono tabele o 90° CW i zweryfikowano **100% wierszy i liczb na s. 16 i s. 17** + notę definicyjną u dołu s. 17 — **0 błędów**. W prześwicie s. 16 widoczne `CONVOCATORIAS, CURSOS Y CURSILLOS` (s. 15 `OCHOANOS`), a na s. 17 `NOTICIARIO NACIONAL` (s. 18 `OCHOANOS`) — fizyczny dowód ciągłości!
7. **`65b525af` (`1wi8oMpk9T3WF9BYIm8Tp8lc1h_MQJIBY`) — `ANEJO Nº 1: INSTITUCIONES PROPIAS`:**
   - Zweryfikowano wszystkie 31 wierszy i kolumnę `PLAZAS` (0 błędów w tabeli MD; zachowano nawet oryginalne `SALAMNCA [sic]`).
   - **WYKRYTY I NAPRAWIONY BŁĄD METADANYCH (linia 10):** W tabeli podsumowującej wpisano `26 instituciones propias`, podczas gdy zarówno na JPG, jak i w samej tabeli Markdown jest dokładnie **31** instytucji. Poprawiono `26` → `31`.

### 3.3. `BOL-ISSUE-UNNUMBERED-995E_ES.md` — **`QA_SPOT_CHECKED`**
- **s. 2–3 (`1tFrdoSU6U4mEAf1JL-MTFaDcAk6XIzT3.jpg`):** *Sumario* (wszystkie 12 pozycji i numery stron `3, 6, 9, 13, 15, 17, 18, 20`), prześwit okładki `AÑO XVIII / NUM. 614 (615) / MADRID`, *Depósito legal*, pełne liczby statystyczne Junta Provincial de Madrid za 1963 r. na s. 3 — **100% zgodne** (wiernie zachowana literówka druku `los numerosos entrañan`).
- **s. 12 (`1z2l9uy9gRzZYhf4vXDX8o_r4gz7WhWpQ.jpg`, lewa połowa obrócona 90° CW):** Zweryfikowano 100% tabeli apaisada (*Tenerife*, *Sevilla*, *Nuevos cursos (en tramitación)*, `253`, `218`, `291`, `229`, `226`) — **0 błędów**.
- **s. 20 (`1DEsggKnA6EYee2lBmDJasMDUcQqHEgXc.jpg`):** Potwierdzono nagłówki obu kongresów (Neapol, Luksemburg) oraz cytat *Marcel Sacotte* — **100% zgodne**.

### 3.4. `BOL-ISSUE-OCHOANOS-UNKNOWN_ES.md` — **`QA_SPOT_CHECKED`**
- **s. 2–3 (`1aiGpRoKYFM0MU-KJwLX3nUR6dherByWc.jpg`):** *Sumario* (wszystkie pozycje `3, 6, 8, 12, 13, 14, 15, 19, 20`), prześwit `AÑO XVII`, cytat *Raquel Payá (1957)*, kursywa wstępna (`15 de enero del año actual`) i *Ocho años de actuación presidencial* (`22 de enero de 1955`, *Manuel Tallada Cuéllar*, *Daoíz, 8*) — **100% zgodne**.
- **s. 6–7 — weryfikacja blokady API (`1cFJalqt6vnjSDeUOOQqAnKKVdigtlBAr.jpg`):**
  - Wizualnie potwierdzono tytuł `Circular de la Fiscalía del Tribunal Supremo sobre el texto revisado del Código Penal en materia de los delitos relativos a la prostitución.`, cytowane przepisy (Decreto-ley 3-III-1956, Circular 31-I-1924, Decreto 24-I-1963 / Ley 23-XII-1962, art. 452 bis, arts. 431, 438 y 439 CP 1944, Ley de Vagos y Maleantes), datę `Madrid, 3 de abril de 1963.` oraz ramkę z cytatem Piusa XII na s. 7.
  - Dokumentacja blokady API jest **100% rzetelna, bez halucynacji i bez obchodzenia filtra**.
- **s. 19 (`1JfURPTwwxMz9UFH4dYTVURWZFVE-Qoqb.jpg`, prawa połowa):** Potwierdzono *Valencia* (z oryginalną literówką `funcional`), *Valladolid*, *Vigo* oraz *Clausura de curso en la Escuela de Reeducadoras* (`28 de junio`, `34 alumnas`, *Tallada*, *Martínez Kleiser*) — **100% zgodne**.

### 3.5. `PRINT-UNKW-INSTITUTION-04-10_ES.md` — **`BLOCKED_VERIFIED_QA_PASS`**
- **s. 4–5 (`1m3RaDqE9Eq3qwVJqhP47OL4LK0zSMLir.jpg`):** Potwierdzono paginację `— 4 —`, `— 5 —`, nagłówki *Alojamiento* (*Dormitorios*, *Comedores*, *Salas de estar y de recreo*), *Muebles y equipo general*, *Personal*, *Personal voluntario*, *Admisión en la institución*.
- **s. 10 + wyklejka tylna (`1e4WoQxnP1zWc8UcdiKCZwVfgQZP7ljRu.jpg`):** Potwierdzono paginację `— 10 —`, nagłówek *Tendencias y problemas principales que se observan en la asistencia institucional a los niños.*, winietę końcową oraz (po wzmocnieniu kontrastu w PIL) odbicie lustrzane stopki `MINISTERIO DE JUSTICIA / BOLETIN DE INFORMACION / REDACCION Y ADMINISTRACION / Ministerio de Justicia - Sección de Publicaciones`.
- Dokumentacja blokady API bez halucynacji i bez obchodzenia filtra — **100% zgodna z protokołem**.

---

## 4. Podsumowanie zmian wprowadzonych bezpośrednio przez QA

1. `/home/antigravity/patronato_closure/stream_b/UNASSIGNED_11_SPREADS_AUDIT_AND_ES.md`:
   - **Krytyczna poprawka metadanych dla `dba54c80` (linia 458):** Usunięto błędną informację, jakoby `BOL-1956-01_Boletin_Num_1_1956-05-05_ES_Claude.md` zawierał pełną transkrypcję s. 6–7; doprecyzowano, że plik Claude'a ma status `INCOMPLETE` (tylko s. 1–5) i że `dba54c80` fizycznie uzupełnia brakujące s. 6–7 (zablokowane obecnie filtrem API).
   - **Poprawka licznika w tabeli głównej dla `65b525af` (linia 10):** `26 instituciones propias` → `31 instituciones propias`.
   - Dodano nagłówek `- **Estado de QA:** QA_SPOT_CHECKED`.
2. Dodano nagłówki `- **Estado de QA:**` do pozostałych 4 plików w `/home/antigravity/patronato_closure/stream_b/`:
   - `GR-UNKNOWN-P03_ATTEMPT_ES.md` → `INDEPENDENT_QA_PASS_FULL`
   - `PRINT-UNKW-INSTITUTION-04-10_ES.md` → `BLOCKED_VERIFIED_QA_PASS`
   - `BOL-ISSUE-UNNUMBERED-995E_ES.md` → `QA_SPOT_CHECKED`
   - `BOL-ISSUE-OCHOANOS-UNKNOWN_ES.md` → `QA_SPOT_CHECKED`

## 5. Bilans końcowy QA (Stream B2)

- **`INDEPENDENT_QA_PASS_FULL`:** 1 plik (`GR-UNKNOWN-P03_ATTEMPT_ES.md`)
- **`BLOCKED_VERIFIED_QA_PASS`:** 1 plik (`PRINT-UNKW-INSTITUTION-04-10_ES.md`)
- **`QA_SPOT_CHECKED`:** 3 pliki (`BOL-ISSUE-UNNUMBERED-995E_ES.md`, `BOL-ISSUE-OCHOANOS-UNKNOWN_ES.md`, `UNASSIGNED_11_SPREADS_AUDIT_AND_ES.md`)
- **`FAIL_NEEDS_FIX`:** 0 plików (2 błędy metadanych w `UNASSIGNED_11_SPREADS_AUDIT_AND_ES.md` naprawione bezpośrednio).
