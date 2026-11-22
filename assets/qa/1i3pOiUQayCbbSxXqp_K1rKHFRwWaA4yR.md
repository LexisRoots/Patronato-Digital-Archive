# RAPORT DOWODOWY NIEZALEŻNEGO QA — STREAM A1 (REWORK 5 KRYTYCZNYCH BŁĘDÓW `FAIL_CRITICAL`)

- **Data audytu:** 2026-11-21
- **Rola:** Niezależny Agent QA (Stream A1)
- **Zakres weryfikacji:** 4 pliki `_v3_REWORK.md` w `/home/antigravity/patronato_closure/stream_a/` (obejmujące 5 pierwotnych jednostek `FAIL_CRITICAL`: `GR-PRINT-1942`, `D45`, `D20`, `GR-PRINT-1943`, `DGS-1546`).
- **Metodyka:**
  - Niezależne obejrzenie wszystkich nieobjętych blokadą API fotografii JPG z `/home/antigravity/patronato_closure/upright/`, obróconych w PIL do pionu (`90° CCW` dla `GR-PRINT-1942+D45`, `180°` dla `D20` i `bd5f5746`) wraz ze zbliżeniami (`3x–4x` Lanczos) numerów telefonów, stopek drukarskich i znaków diakrytycznych.
  - Porównanie **słowo po słowie i znak po znaku** tekstu transkrypcji z oryginalnym obrazem.
  - Weryfikacja linków Google Drive i nazw plików przeciwko `/home/antigravity/patronato_closure/jpg_manifest.json` oraz `/home/antigravity/patronato_closure/existing_tx/`.
  - Dla plików zablokowanych przez filtr praw autorskich API (`1o72FZwCLIuMJz-uyo6UDL9Nt1pf6wJtV.jpg`, `1Kya2o8sBiEbbMOuyu3KW130YUBSVoLfA.jpg`, `1TOfueHnMA71l_6Ss9B5e5ugjAPihe-mX.jpg`): weryfikacja wyłącznie metadanych, linków, istnienia plików w repozytorium oraz poprawności udokumentowania blokady bez halucynacji i bez obchodzenia filtra.

---

## Tabela zbiorcza werdyktów QA

| # | Jednostka (v7) | Plik `_v3_REWORK.md` | Źródłowe JPG | Werdykt QA | Uwagi kluczowe |
|---|---|---|---|---|---|
| 1 | `GR-PRINT-1942+D45` (cat. `009`) | `GR-PRINT-1942_D45_Circular_1942_ES_v3_REWORK.md` | `1fMduE36ch-pZTHHXlEvXOMJWCZPawEBQ.jpg` (p. 1), `1WMIZB4VVl6EOcJ0ptswaW57wshlaxzho.jpg` (p. 2) | **`INDEPENDENT_QA_PASS_FULL`** | 100% zgodności słowo po słowie na obu stronach; wszystkie 5 nazwisk wykładowców, daty, liczby i Sekcja D zweryfikowane na zbliżeniach. |
| 2 | `D20` (cat. `011`) | `D20_ES_v3_REWORK.md` | `1oeJcl9FUZqShBJ_ilWlofkshZ-VgTd9F.jpg` | **`INDEPENDENT_QA_PASS_FULL`** | 100% zgodności słowo po słowie (w tym `advirtiéndolos`, `TÉCNICO`, `A. Martín Artajo.`); stopka `DIANA` poprawnie oznaczona w Sekcji D (`PRINT_CONF: LOW`). |
| 3 | `GR-PRINT-1943` (cat. `012`) | `GR-PRINT-1943_Circular_3_1943_ES_v3_REWORK.md` | `bd5f5746-f8e8-4b41-b21c-8fb7947bfff0.jpg` (p. 4 — zweryfikowana), `1o72FZwCLIuMJz-uyo6UDL9Nt1pf6wJtV.jpg` (zablokowana API) | **`INDEPENDENT_QA_PASS_FULL` (p. 4 `bd5f5746`, po korekcie QA `reuna` → `reúna`) + `BLOCKED_VERIFIED_QA_PASS` (p. `38fdd7b0`)** | Na zbliżeniu `bd5f5746` wykryto i natychmiast poprawiono brak akcentu `se reuna` → `se reúna` (linia 54). Po korekcie 100% zgodności str. 4; blokada API dla `38fdd7b0` udokumentowana rzetelnie bez halucynacji i bez obchodzenia filtra. |
| 4 | `DGS-1546` (cat. `010`) | `DGS-1546_Circular_Playas_Piscinas_ES_v3_REWORK.md` | `1Kya2o8sBiEbbMOuyu3KW130YUBSVoLfA.jpg` (Ej. A), `1TOfueHnMA71l_6Ss9B5e5ugjAPihe-mX.jpg` (Ej. B) | **`BLOCKED_VERIFIED_QA_PASS`** | Oba linki Drive i metadane zgodne z `jpg_manifest.json` (poprawiony błędny link Ej. A ze starej wersji); blokada filtra API udokumentowana dokładnie, bez halucynacji i bez obchodzenia filtra. |

---

## Szczegółowe dowody weryfikacji (pozycja po pozycji)

### 1. `GR-PRINT-1942+D45` — `GR-PRINT-1942_D45_Circular_1942_ES_v3_REWORK.md`
- **Werdykt:** **`INDEPENDENT_QA_PASS_FULL`**
- **Zweryfikowane obrazy:**
  - Str. 1: `/home/antigravity/patronato_closure/upright/1fMduE36ch-pZTHHXlEvXOMJWCZPawEBQ.jpg` (obrót 90° CCW + zbliżenie 4× na nagłówek prawy)
  - Str. 2: `/home/antigravity/patronato_closure/upright/1WMIZB4VVl6EOcJ0ptswaW57wshlaxzho.jpg` (obrót 90° CCW)
- **Zweryfikowane metadane i linki:**
  - Teczka archiwalna widoczna na obu zdjęciach: `AHPTO 15429` / `AC 2949/3`, `Junta de Comunidades de Castilla-La Mancha — Consejería de Educación y Cultura`, rękopis: `Patronato de Protección a la Mujer / Circulares` — **ZGODNE**.
  - Linki Drive: `1fMduE36ch-pZTHHXlEvXOMJWCZPawEBQ` (p. 1, `ec8af053-f617-49aa-8a51-d7c3fe882667.jpg`) i `1WMIZB4VVl6EOcJ0ptswaW57wshlaxzho` (p. 2, `376a5ccd-5ff8-4d13-9f95-2524c87d641e.jpg`) — **ZGODNE** z `jpg_manifest.json`.
- **Zweryfikowane nazwiska, daty, liczby i nagłówki:**
  - Nagłówek lewy: `MINISTERIO DE JUSTICIA` / `PATRONATO DE PROTECCIÓN A LA MUJER` — **ZGODNE**.
  - Nagłówek prawy: `NUÑEZ DE BALBOA, 31` (bez akcentu w `NUÑEZ` — wiernie!), `TELÉF. [lectura dudosa: 51929]` (zbliżenie 4× potwierdza niewielki, lekko rozmyty druk cyfr — poprawnie oznaczono `PRINT_CONF: MEDIUM` z alternatywami `51829` / `51928` w Sekcji D), `MADRID` — **ZGODNE**.
  - Tytuł: `Circular n.° 2.` (podkreślony), adresat: `A LAS JUNTAS PROVINCIALES:` — **ZGODNE**.
  - Daty i liczby (str. 1): `el día 20 de este mes`; `Boletín Oficial del Estado del 25 del pasado octubre`; `a partir del próximo día 21, y por tiempo de un mes`; punkt `1.° MORAL.` — **ZGODNE**.
  - Nazwiska wykładowców (str. 2):
    1. `D. José Collado, cura párroco de Tetuán de las Victorias, Consiliario del Patronato.` — **ZGODNE**.
    2. `Doctor Don Francisco Javier Echalecu y Canino, profesor auxiliar de Psicopatología de la Facultad de Medicina de Madrid y Jefe del Servicio Médico del Patronato.` — **ZGODNE** (usunięto halucynację `José Mallart`).
    3. `D. José Rodríguez Soler, letrado consistorial y profesor auxiliar de Política social en la Universidad Central.` — **ZGODNE** (usunięto halucynację `Gregorio Santiago y Castiella`).
    4. `Señorita Elisa Barraquer, maestra y vocal de este Patronato.` — **ZGODNE** (usunięto halucynację `Mariano Yela Granizo`).
    5. `Señorita María Sabater, Directora de la Escuela Social y Familiar de la mujer; señorita María Hernández Lázaro.` — **ZGODNE** (usunięto halucynację `Salvador Escala Miliá`).
  - Daty i liczby (str. 2): `Presupuestos de 1943`; `Real Decreto del Ministerio de la Gobernación de 3 de Diciembre de 1903`; `Circular n.° 1`; `los sábados a las cuatro y media de la tarde`; `Madrid, 12 de noviembre de 1942.` — **ZGODNE**.
  - Podpis: `El Vicepresidente,` / `*A. Martín Artajo* [firma impresa en facsímil]` (brak kropki po nazwisku w faksymile — wiernie!) — **ZGODNE**.
  - Stopka drukarska: brak na obu stronach — **ZGODNE**.
- **Błędy wykryte:** brak (`0`).

---

### 2. `D20` — `D20_ES_v3_REWORK.md`
- **Werdykt:** **`INDEPENDENT_QA_PASS_FULL`**
- **Zweryfikowany obraz:**
  - `/home/antigravity/patronato_closure/upright/1oeJcl9FUZqShBJ_ilWlofkshZ-VgTd9F.jpg` (obrót 180° + zbliżenie 3× na stopkę drukarską w prawym dolnym rogu)
- **Zweryfikowane metadane i linki:**
  - Teczka archiwalna: `AHPTO 15429` / `AC 2949/3` — **ZGODNE**.
  - Link Drive: `1oeJcl9FUZqShBJ_ilWlofkshZ-VgTd9F` (`0e690475-f908-4aaf-8092-bdb340d604ac.jpg`) — **ZGODNE** z `jpg_manifest.json`.
  - Delimitacja kadru (`PHOTO_SCOPE: HIGH`): prawidłowe oddzielenie dokumentu `D20` od podłożonej sąsiedniej kartki po prawej stronie (z fragmentami `-TALLERES`, `3.-LA MO...`).
- **Zweryfikowane nazwiska, daty, liczby i stopka:**
  - 4 wiersze otwierające (końcówka punktu 6): `cial nos ha pedido... advirtiéndolos... prohibida la venta de otros tipos.` — **ZGODNE** (wiernie zachowane `advirtiéndolos`).
  - Punkt `7.`: nagłówek bez akcentów `INTERVENCION` / `SUSPENSION` — wiernie; treść `Con las debidas reservas... mayores de dieciséis años y menores de veintitrés.` — **ZGODNE** (usunięto halucynację o `Comisión de Legislación`).
  - Punkt `8.`: nagłówek `8.-NOMBRAMIENTO DE SECRETARIO TÉCNICO.` (z akcentem na `TÉCNICO` — wiernie!); nazwisko `don José María Sánchez de Muniain Gil.` — **ZGODNE**.
  - Punkt `9.`: `9.-CARNETS Y EMBLEMA.` — jednozdaniowy akapit — **ZGODNE**.
  - Punkt `10.`: `10.-SESIONES DE LA JUNTA NACIONAL.` — `los sábados` → `los martes, a las cuatro y media de la tarde` — **ZGODNE** (usunięto halucynację o `Carmen Polo de Franco`).
  - Data i podpis: `Madrid, 10 de marzo de 1943.` / `El Vicepresidente,` / `*A. Martín Artajo.* [firma impresa en facsímil]` (z kropką po nazwisku — wiernie!) — **ZGODNE**.
  - Stopka drukarska (zbliżenie 3×): drobny, lekko nieostry napis jednolinijkowy pod krótką poziomą kreską (`DIANA, S. A. MADRID` / `DIANA, A. G. MADRID`). Poprawnie oznaczono `[lectura dudosa: DIANA, S. A. MADRID]` z `PRINT_CONF: LOW` i alternatywą `DIANA, A. G. MADRID` w tabeli Sekcji D (usunięto zmyśloną stopkę `GRÁFICAS UGUINA`).
- **Błędy wykryte:** brak (`0`).

---

### 3. `GR-PRINT-1943` — `GR-PRINT-1943_Circular_3_1943_ES_v3_REWORK.md`
- **Werdykt:** **`INDEPENDENT_QA_PASS_FULL` (p. 4 `bd5f5746`, po korekcie QA) + `BLOCKED_VERIFIED_QA_PASS` (`38fdd7b0`)**
- **Część A — Strona 4 (`bd5f5746-f8e8-4b41-b21c-8fb7947bfff0.jpg`):**
  - **Zweryfikowany obraz:** `/home/antigravity/patronato_closure/upright/bd5f5746-f8e8-4b41-b21c-8fb7947bfff0.jpg` (obrót 180° + zbliżenie 3× na stopkę drukarską oraz zbliżenie 3× na wiersz `se reúna semanalmente`).
  - **Link Drive:** `1kM6BBwWB7QHiBLiKNdCiQ2rjpRIt8ByQ` — **ZGODNY** z `jpg_manifest.json`.
  - **Wykryty i naprawiony błąd QA:**
    - W linii 54 pliku transkrypcji widniało `se reuna semanalmente` (bez akcentu nad `u`). Zbliżenie 3× oryginalnego obrazu jednoznacznie potwierdza obecność akcentu ostrego: **`se reúna semanalmente`**.
    - **Działanie naprawcze QA:** poprawiono bezpośrednio w `/home/antigravity/patronato_closure/stream_a/GR-PRINT-1943_Circular_3_1943_ES_v3_REWORK.md` (linia 54: `reuna` → `reúna`).
  - **Pozostałe elementy zweryfikowane słowo po słowie:**
    - Nagłówki `10.-SIGILO PROFESIONAL` i `11.-INFORMES PARA LA FUTURA MEMORIA` (oba podkreślone, bez kropki końcowej — wiernie!).
    - Formy literalne `sólo`, `transcienda`, `aun`, `ésta`, `(otoño de 1942)`, `Comisarios Jefes de Policía` — **ZGODNE**.
    - Data i podpis: `Madrid, 17 de junio de 1943.` / `EL VICEPRESIDENTE,` (wersaliki) / `A. Martín Artajo.` (pismo drukowane standardowe, nie faksymile odręczne — wiernie odnotowane w Sekcji D!) — **ZGODNE**.
    - Stopka drukarska (zbliżenie 3×): pod krótką kreską poziomą widoczne `Imp. Sáez - Madrid`; ostrożnie oznaczone jako `[lectura dudosa: Imp. Sáez - Madrid]` (`PRINT_CONF: MEDIUM`, alternatywa `Imp. Idea - Madrid`) — **ZGODNE** z Sekcją D.
- **Część B — Strona zablokowana (`38fdd7b0-c29c-4209-b014-7cb717f7dab0.jpg`):**
  - **Link Drive i plik lokalny:** `https://drive.google.com/file/d/1o72FZwCLIuMJz-uyo6UDL9Nt1pf6wJtV/view` — **ZGODNY** z `jpg_manifest.json`, plik obecny w `upright/` (`316055` B).
  - **Dokumentacja blokady API:** zapisano dokładny komunikat filtra praw autorskich API (`response blocked by content safety filters: ... existing copyrighted works`), nie podjęto próby obejścia filtra ani parafrazy zastępczej, brak halucynacji tekstu, zachowano rzetelną notę archiwalną o rozdzieleniu dokumentów z 17.06.1943 i 7/16.08.1943 do katalogu v8.

---

### 4. `DGS-1546` — `DGS-1546_Circular_Playas_Piscinas_ES_v3_REWORK.md`
- **Werdykt:** **`BLOCKED_VERIFIED_QA_PASS`**
- **Zweryfikowane metadane i linki:**
  - Ejemplar A (`799d093f-915c-4cb6-9453-f5c345843d25.jpg`): `https://drive.google.com/file/d/1Kya2o8sBiEbbMOuyu3KW130YUBSVoLfA/view` — **ZGODNY** z `jpg_manifest.json` (plik obecny w `upright/`, `373391` B; naprawiono błędny link `1FfZCmh9d7LmaaBTACkwIURrbk2cAfl7-` ze starego pliku `existing_tx`).
  - Ejemplar B (`a83be5c7-cfb2-401f-bc88-a41db46b5654.jpg`): `https://drive.google.com/file/d/1TOfueHnMA71l_6Ss9B5e5ugjAPihe-mX/view` — **ZGODNY** z `jpg_manifest.json` (plik obecny w `upright/`, `299324` B).
  - Signatura archiwalna `AHPTO 15429` / `AC 2949/3` i identyfikator `DGS-1546` (cat. `010`) — **ZGODNE**.
- **Weryfikacja dokumentacji blokady API:**
  - Dokładny komunikat blokady filtra bezpieczeństwa API przytoczony dosłownie.
  - Status `BLOCKED_API_COPYRIGHT_FILTER` jawnie oznaczony; brak jakiejkolwiek próby obejścia filtra lub halucynowania tekstu literalnego.
  - Poprawnie udokumentowano błąd `FAIL_CRITICAL` w starym pliku (podmieniony tekst zaczynający się od *„Restaurado el Patronato...”*) oraz rzetelnie wskazano ścieżkę zamknięcia (transkrypcja ludzka lub OCR nieobjęty filtrem recytacji, z Ejemplar A jako bazą główną).
