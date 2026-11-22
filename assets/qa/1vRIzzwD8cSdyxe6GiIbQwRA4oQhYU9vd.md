# Raport Dowodowy Niezależnego QA — Stream A2 (Korekty Claude, C16/C22/C28 i 8 plików Claude)

**Data weryfikacji:** 2026-11-21  
**Rola:** Niezależny Agent QA (Stream A2)  
**Metodologia:** Bezpośrednia weryfikacja wizualna przeciwko oryginalnym fotografiom JPG z `/home/antigravity/patronato_closure/upright/` (obróconym do pozycji czytania i powiększonym przez PIL ×2–×4 dla detali krytycznych: nagłówków, dat, nadruków, stempli, adresów i granic ciągłości) oraz krzyżowe sprawdzenie z `MASTER_CATALOG_PATRONATO_ALMU_v7.json` i katalogiem `/home/antigravity/patronato_closure/claude/`.

---

## 1. Tabela werdyktów QA (Stream A2)

| # | Plik w `/home/antigravity/patronato_closure/stream_a/` | Zweryfikowane JPG / Źródła | Werdykt QA | Podsumowanie ustaleń |
|---|---|---|---|---|
| 1 | `D14_Circular_6_194X_ES_v2_CORRECTED.md` | `190OwPyxYKvR7oiyowvVHzYQb4PgS3tHv.jpg` (obrót 180°, PIL ×3/×4) | **`INDEPENDENT_QA_PASS_FULL`** | Numer `Circular n.º 6.` potwierdzony bezspornie; rok `194[?] [lectura dudosa: 1943/1945]` bez zgadywania; komplet pól Sekcji D; pełny tekst zgodny słowo po słowie z JPG. |
| 2 | `D49_Circular_57_1959-11-01_ES_v2_CORRECTED.md` | `1dN-oWG8Mdyp5HVN6SoWV5_JqrrzwiQZK.jpg` (s. 1), `1mgObiZ7DUaKLxTurH6Zs21FCzVnqhf8h.jpg` (s. 2) (obrót 90° CCW, PIL ×4) | **`INDEPENDENT_QA_PASS_FULL`** | Adres `NUÑEZ DE BALBOA, 33` potwierdzony na **obu** stronach (pod spodem wystaje inna kartka z `...BOA, 35`); stempel wyjścia, data `1º de Noviembre de 1959`, tekst obu stron i pola Sekcji D zweryfikowane. |
| 3 | `D51_Circular_71_1965-01-25_ES_v2_CORRECTED.md` | `1n88tOq_u816WPa21APAVsZWxqqk5nlNd.jpg` (obrót 90° CCW, PIL ×4) | **`INDEPENDENT_QA_PASS_FULL`** | Wyraźne sobremecanografiado `24→25` w dacie (`OVERPRINT_CONF: MEDIUM`); druga cyfra dnia w stemplu wejścia Toledo faktycznie nieczytelna/wątpliwa (`[lectura dudosa: 2?-1-1965]`, `STAMP_CONF: LOW`); adres `NUÑEZ DE BALBOA, 35` i pełny tekst zgodne z JPG. |
| 4 | `NEW-C08_plus_D53_Circular_8_1944-09_ES_v2_MERGED.md` | `16FxchgGTs90CzemgvL5tUX0yucDrAelp.jpg` (s. 1, prawa strona po 180°), `1xfs59kahw1XkxF5vbVGFaYAZsB-2hjrA.jpg` (s. 2 / `D53`, środek po 180°) | **`INDEPENDENT_QA_PASS_FULL`** | Ciągłość tekstu między s. 1 (*El examen de entrada consistirá en un ejercicio oral y otro escrito.*) a s. 2 (*El ejercicio oral constará de tres partes, a saber:*) potwierdzona wizualnie; zachowany alias `D53`; usunięte błędne powiązanie z `D15` (Circular n.º 5); pełny tekst obu stron zweryfikowany z JPG. |
| 5 | `C07-1940s_Circular_7_Anexo_I_II_1944-02-22_ES_v2_CANONICAL.md` | `16FxchgGTs90CzemgvL5tUX0yucDrAelp.jpg` (środek po 180° = Anexo II) + metadane v7 | **`QA_SPOT_CHECKED`** | Sprzeczna notatka o braku Anexo II usunięta; dodany `16FxchgGTs90CzemgvL5tUX0yucDrAelp` i precyzyjny `PHOTO_SCOPE`; tekst Anexo II zweryfikowany słowo po słowie z JPG. Status `QA_SPOT_CHECKED` (zgodnie z samym plikiem) — pełne drugie czytanie s. 1–3 (`5d45dac2`, `20e7c9bd`) nie było przedmiotem delty A2. |
| 6a | `C16-1945_Circular_16_1945_ES_v2_CANONICAL.md` | `1nxw6p6KbCztqX7NCIZQN8K47xHPYuBKt.jpg` (obrót 180°) + katalog v7 | **`INDEPENDENT_QA_PASS_FULL`** | Wyłącznie po hiszpańsku (brak tekstu EN); link JPG 100% zgodny z katalogiem v7; pełny tekst zgodny słowo po słowie z JPG. |
| 6b | `C22-1946_Circular_22_1946_ES_v2_CANONICAL.md` | `1E3uf7iaIB6R4RNy5NIcgpHLPuRq6Sw6G.jpg` (obrót 90° CCW) + katalog v7 | **`INDEPENDENT_QA_PASS_FULL`** | Wyłącznie po hiszpańsku (brak tekstu EN); link JPG 100% zgodny z katalogiem v7; pełny tekst zgodny słowo po słowie z JPG. |
| 6c | `C28-1948_Circular_28_1948_ES_v2_CANONICAL.md` | `1RxwT4XjAqn_e48IbeWTVY-Mu9GEoiGJK.jpg` (obrót 90° CCW, PIL ×2) + katalog v7 | **`INDEPENDENT_QA_PASS_FULL`** | Wyłącznie po hiszpańsku (brak tekstu EN); link JPG 100% zgodny z katalogiem v7; korekta `pero límite al mismo tiempo de los abusos` **potwierdzona w 100%** na powiększeniu PIL ×2; pełny tekst zgodny z JPG. |
| 7 | `CLAUDE_8_FILES_RECONCILIATION.md` | 8 plików w `/home/antigravity/patronato_closure/claude/` + katalog v7 | **`QA_SPOT_CHECKED`** | Rozliczenie wszystkich 8/8 plików Claude poprawne merytorycznie (kompletność, linki JPG, statusy `INCOMPLETE` dla `BOL-1956-01` i `194[2/3]` dla `GR-PRINT-ANNEX-C04`). **Uwaga drobna:** w wierszu 6 tabeli pominięto człon `_Celadoras_` w ID katalogu v7 (wpisano `17_NEW-C24_Circular_24_1947-10-17_ES` zamiast rzeczywistego `17_NEW-C24_Circular_24_Celadoras_1947-10-17_ES`). |

---

## 2. Szczegółowe dowody weryfikacji wizualnej (punkt po punkcie)

### 2.1. `D14_Circular_6_194X_ES_v2_CORRECTED.md` (`190OwPyxYKvR7oiyowvVHzYQb4PgS3tHv.jpg`)
- **Nagłówek (PIL ×3):** Wyraźnie widoczne podkreślone `Circular n.º 6.` (poprzedni błąd `8` usunięty).
- **Data (PIL ×4):** `Madrid, 7 de diciembre de 194?.` — czwarta cyfra ma dolny łuk przypominający `3`, lecz górny fragment jest spłaszczony/rozmazany na granicy między `3` a `5`. Zapis `194[?] [lectura dudosa: 1943/1945]` bez zgadywania roku spełnia reguły Sekcji D.
- **Pola Sekcji D:** Obecne wszystkie wymagane pola (`PRINT_CONF`, `OVERPRINT_CONF`, `STAMP_CONF`, `HANDWRITING_CONF`, `PHOTO_SCOPE`) wraz z podpolami `jpg_url`, `location`, `literal_reading`, `alternative_reading`, `reason`, `review_status`.
- **Pełny tekst:** Zweryfikowany akapit po akapicie z obróconym JPG (zachowane `pués`, `órden`, `Ordenes`, wyodrębniony wystający u dołu fragment Circular núm. 7 `b) Que, por ser huérfana...`).
- **Drobna uwaga redakcyjna (nieblokująca):** Pod `EL VICEPRESIDENTE,` widnieje drukowany podpis kursywą `A. Martín Artajo.` bez osobnej parafki pod spodem — zapis `[rúbrica impresa]` odnosi się do faksymilowego druku nazwiska.

### 2.2. `D49_Circular_57_1959-11-01_ES_v2_CORRECTED.md` (`1dN-oWG8Mdyp5HVN6SoWV5_JqrrzwiQZK.jpg` i `1mgObiZ7DUaKLxTurH6Zs21FCzVnqhf8h.jpg`)
- **Adres w nagłówku (PIL ×4, s. 1 i s. 2):** Na obu stronach w prawym górnym rogu arkusza głównego wyraźnie wydrukowane `NUÑEZ DE BALBOA, 33`. Tuż na prawo, spod stosu wystaje krawędź innego dokumentu z widocznym fragmentem `...BOA, 35`, co wyjaśnia pierwotny błąd v1.
- **Stempel wyjścia (s. 1):** Niebieski prostokątny stempel `PATRONATO DE PROTECCION A LA MUJER / MINISTERIO DE JUSTICIA / SALIDA / N.º 1985 / 29 de Octbre de 1959` potwierdzony.
- **Treść s. 1 i s. 2:** Zweryfikowana z pełnymi obróconymi stronami (m.in. zachowane `Couta Sindical Obrera.`, `Madrid, 1º de Noviembre de 1959`, podpis `[ilegible]`). Drobna normalizacja literówek maszynowych oryginału (`Estadoy` → `Estado y`, `Institutp` → `Instituto`) — nieblokująca.

### 2.3. `D51_Circular_71_1965-01-25_ES_v2_CORRECTED.md` (`1n88tOq_u816WPa21APAVsZWxqqk5nlNd.jpg`)
- **Sobremecanografiado w dacie (PIL ×4):** W linii `Madrid, 25 de enero de 1965` pod cyfrą `5` wyraźnie przebija pierwotnie wybita cyfra `4`. Zapis `25 [sobremecanografiado: 24→25]` oraz pole `OVERPRINT_CONF: MEDIUM` w pełni uzasadnione i potwierdzone.
- **Stempel wejścia w Toledo (PIL ×4):** W niebieskim stemplu `ENTRADA nº 12 / Fecha 2?-1-1965` druga cyfra dnia jest napisana ręcznie niewyraźnym, poprawianym pociągnięciem (możliwe `7`, `9` lub `3`). Oznaczenie `[lectura dudosa: 2?-1-1965]` oraz `STAMP_CONF: LOW` / `HANDWRITING_CONF: LOW` jest wzorcowe.
- **Stempel wyjścia i adres:** `SALIDA Nº 328 / 25 DE 1 DE 1965` oraz `NUÑEZ DE BALBOA, 35` potwierdzone.
- **Pełny tekst:** Zweryfikowany słowo po słowie (drobna literówka maszynopisu `Patrpnato` w 1. wierszu znormalizowana do `Patronato`).

### 2.4. `NEW-C08_plus_D53_Circular_8_1944-09_ES_v2_MERGED.md` (`16FxchgGTs90CzemgvL5tUX0yucDrAelp.jpg` i `1xfs59kahw1XkxF5vbVGFaYAZsB-2hjrA.jpg`)
- **Granica ciągłości (PIL ×2):**
  - Koniec s. 1 (`16Fxchg...jpg`, prawa karta po obrocie 180°): `Tercera. Habrá tres pruebas eliminatorias, a saber: un examen de entrada, otro al final del primer mes de estudios y otro al final de curso.` / `El examen de entrada consistirá en un ejercicio oral y otro escrito.`
  - Początek s. 2 (`1xfs59k...jpg`, środkowa karta po obrocie 180°): `El ejercicio oral constará de tres partes, a saber:` / `a) Explicar un capítulo del Catecismo del P. Ripalda o del P. Astete y desarrollar alguno de sus puntos.`
  - Identyczny krój kursywy drukarskiej, papier, układ typograficzny i chronologia (`20`/`25`/`27 de septiembre de 1944`).
- **Metadane i alias:** Alias `D53` zachowany jawnie; błędne powiązanie z `D15` (Circular n.º 5) oraz błędny opis „segundo curso” całkowicie usunięte.
- **Pełny tekst obu stron:** Zweryfikowany z obróconymi JPG (włącznie ze stopką drukarską `Papelería Madrileña.-Mayor, 36.-Madrid`).

### 2.5. `C07-1940s_Circular_7_Anexo_I_II_1944-02-22_ES_v2_CANONICAL.md` (`16FxchgGTs90CzemgvL5tUX0yucDrAelp.jpg`)
- **Usunięcie sprzeczności:** W metadanych brak jakiejkolwiek sprzecznej notatki o braku Anexo II; status ustawiony jako `COMPLETE` (4 strony na 3 fotografiach).
- **Dodanie źródła i `PHOTO_SCOPE`:** Dodano `755048e3-f916-492f-bc13-0c708b944eeb.jpg` (`16FxchgGTs90CzemgvL5tUX0yucDrAelp`) z czytelnym rozgraniczeniem `PHOTO_SCOPE` (lewa = teczka, środek = Anexo II `C07-1940s`, prawa = `NEW-C08`).
- **Weryfikacja wizualna Anexo II:** Cały tekst `Anexo II` (od `Expediente núm.` / `Sobre` po `Sr. Juez de Instrucción de este Partido.`) zweryfikowany słowo po słowie przeciwko obróconemu kadrowi `16Fxchg...jpg`. Wszystkie trzy frazy oznaczone ostrożnościowo jako `[lectura dudosa: ...]` (`progenitores o actuales guardadores legales`, `causantes o explotadores`, `reeducada`) potwierdzają się na powiększeniu.
- **Zakres werdyktu:** Ponieważ s. 1–3 (`5d45dac2`, `20e7c9bd`) nie były poddawane pełnej weryfikacji słowo-po-słowie w ramach tej kontroli, utrzymujemy uczciwy werdykt **`QA_SPOT_CHECKED`**.

### 2.6. `C16-1945`, `C22-1946`, `C28-1948` (`*_ES_v2_CANONICAL.md`)
- **Język:** Wszystkie 3 pliki są **wyłącznie po hiszpańsku** (brak tłumaczeń i komentarzy prozą po angielsku; jedynie standardowe etykiety techniczne statusów typu `COMPLETE`, `HIGH`, `N/A` oraz odwołania do nazw historycznych plików draft).
- **Zgodność linków JPG z `MASTER_CATALOG_PATRONATO_ALMU_v7.json`:**
  - `C16-1945`: `68fa391d-7544-4f0b-ba5b-93b354a467b7.jpg` (`1nxw6p6KbCztqX7NCIZQN8K47xHPYuBKt`) — **100% zgodny**.
  - `C22-1946`: `6ba9cc79-c966-40c4-9458-33cd9673b9a2.jpg` (`1E3uf7iaIB6R4RNy5NIcgpHLPuRq6Sw6G`) — **100% zgodny**.
  - `C28-1948`: `54c828ac-d9f7-49d6-8ca8-af3267071300.jpg` (`1RxwT4XjAqn_e48IbeWTVY-Mu9GEoiGJK`) — **100% zgodny**.
- **Kluczowa korekta w `C28-1948` (`1RxwT4XjAqn_e48IbeWTVY-Mu9GEoiGJK.jpg`, PIL ×2):** W 3. akapicie oryginał maszynopisu brzmi dokładnie: `compatible con todas las diversiones, pero límite al mismo tiempo de los abusos` (bez słowa `que`, z `de los abusos`). Korekta w `C28-1948_Circular_28_1948_ES_v2_CANONICAL.md` jest w **100% trafna**.
- **Pełne sprawdzenie tekstu:** Wszystkie trzy jednostronicowe okólniki (`C16-1945`, `C22-1946`, `C28-1948`) zweryfikowano w całości słowo po słowie z obróconymi JPG — brak błędów merytorycznych.

### 2.7. `CLAUDE_8_FILES_RECONCILIATION.md`
- **Kompletność rozliczenia:** Wszystkie 8 plików z `/home/antigravity/patronato_closure/claude/*_ES_Claude.md` ujęte w tabeli.
- **Zgodność linków JPG z v7:** Zweryfikowana programowo — 6 niezmienionych plików (`GR-PRINT-ANNEX-C04`, `D04`, `D01`, `NEW-C24`, `D40`, `BOL-1956-01`) ma 100% zgodności Drive ID z `MASTER_CATALOG_PATRONATO_ALMU_v7.json`, a dla `C07-1940s` i `NEW-C08` prawidłowo wskazano dodanie `16Fxchg...` i scalenie z `D53` (`1xfs59k...`).
- **Zgodność statusów z oryginałami Claude:** Potwierdzono `INCOMPLETE / PENDING_PHOTO` dla `BOL-1956-01` (brak s. 6+ z końcówką pkt 10 i Circular núm. 47) oraz `194[2/3] YEAR_UNCERTAIN / PENDING_PHOTO` dla `GR-PRINT-ANNEX-C04`.
- **Drobny błąd do poprawy przy aktualizacji v8:** W wierszu 6 kolumna `ID w katalogu v7` podaje `17_NEW-C24_Circular_24_1947-10-17_ES`, podczas gdy dokładny klucz `doc_id` w `MASTER_CATALOG_PATRONATO_ALMU_v7.json` to **`17_NEW-C24_Circular_24_Celadoras_1947-10-17_ES`**.

---

## 3. Bilans końcowy QA (Stream A2)

- **`INDEPENDENT_QA_PASS_FULL`:** 7 plików (`D14`, `D49`, `D51`, `NEW-C08+D53`, `C16-1945`, `C22-1946`, `C28-1948`).
- **`QA_SPOT_CHECKED`:** 2 pliki (`C07-1940s` — Anexo II i delta A2 w pełni zweryfikowane, s. 1–3 do pełnego 2. czytania; `CLAUDE_8_FILES_RECONCILIATION.md` — merytorycznie poprawne, 1 literówka w ID v7 dla wiersza 6 `17_NEW-C24_Circular_24_Celadoras_1947-10-17_ES`).
- **`FAIL_NEEDS_FIX`:** 0 plików.
