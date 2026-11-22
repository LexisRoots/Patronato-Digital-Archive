# Niezależny Raport QA — Integracja 6 nowych transkrypcji Claude (22.11.2026)

- **Data audytu:** 2026-11-22
- **Audytor:** Niezależny Agent QA (niebędący autorem transkrypcji)
- **Zakres:** 6 plików z `/home/antigravity/patronato_closure/claude_7/` zweryfikowanych niezależnie przeciwko 10 oryginalnym fotografiom JPG z `/home/antigravity/patronato_closure/upright/` (obróconym do pionu i pociętym w PIL na osobne strony i półstrony w wysokiej rozdzielczości).
- **Metodyka:** Kontrola kolumna po kolumnie i linia po linii (nagłówki, daty, numery artykułów, kwoty kar, progi wiekowe, listy państw, ciągłość między stronami, odczyty niepewne, warianty egzemplarzy oraz elementy pozatekstowe / przebicia druku).

---

## Tabela zbiorcza werdyktów QA

| # | Plik transkrypcji (`claude_7/`) | Fotografie źródłowe (`upright/`) | Werdykt QA | Błędy / uwagi krytyczne |
|---|---|---|---|---|
| 1 | `DGS-1546_Circular_DGS_1546_playas_ES_Claude.md` | `1Kya2o8sBiEbbMOuyu3KW130YUBSVoLfA.jpg` (Ej. A, 180°), `1TOfueHnMA71l_6Ss9B5e5ugjAPihe-mX.jpg` (Ej. B, 90° CCW) | **`INDEPENDENT_QA_PASS_FULL`** | 0 błędów wobec Ej. A; potwierdzono brak daty na obu kopiach i rozbieżność 15.06.1942 vs 18.06.1942. |
| 2 | `GR-PRINT-1943_pagina_agosto_38fdd7b0_ES_Claude.md` | `1o72FZwCLIuMJz-uyo6UDL9Nt1pf6wJtV.jpg` (180°) | **`INDEPENDENT_QA_PASS_FULL`** | 0 błędów; daty, adres i 1 niepewny akcent (`constituído/constituido`) zweryfikowane. |
| 3 | `BOL-1963-05_pp4-10_Convenio_ONU_y_Reforma_CP_ES_Claude.md` | `1dIuNM6us8xxuuPyyz33WuuMsWiOTaX_d.jpg` (s. 4–5), `1R0qmYJG45RFWbllkc9trQ2rOoqObIKoN.jpg` (s. 6–7), `1I1PhCRSYgNDUmhwg4_13ELJzQZUG1tTK.jpg` (s. 8–9), `12hNT_n1N5djB94eZFOF3PZsWqPbQCKf0.jpg` (s. 10–11) (wszystkie 180°) | **`INDEPENDENT_QA_PASS_FULL`** (1 drobna literówka do poprawy w l. 257) | 100% zgodności wszystkich 28 art. Konwencji, 29 państw/dat i wszystkich art./kar reformy KK; 1 drobny błąd przy podziale wyrazu: l. 257 `comprende de` → `comprende`. |
| 4 | `BOL-OCHOANOS_pp6-7_Circular_Fiscalia_TS_1963-04-03_ES_Claude.md` | `1cFJalqt6vnjSDeUOOQqAnKKVdigtlBAr.jpg` (180°) | **`INDEPENDENT_QA_PASS_FULL`** | 0 błędów; kolejność linii na wygiętej karcie 100% poprawna; ramka Piusa XII uczciwie opisana bez pełnej transkrypcji. |
| 5 | `BOL-1956-01_pp6-7_Orden_fin_y_Circular_47_ES_Claude.md` | `dba54c80-d1e6-43a6-99c2-f8d9c9facf62.jpg` (180°) | **`INDEPENDENT_QA_PASS_FULL`** (**cały numer: `COMPLETE`**) | 0 błędów merytorycznych; **jednoznaczny dowód wizualny**, że numer kończy się na s. 7 (na odwrocie przebija tylna okładka). |
| 6 | `a4d541c9_Boletin_1956_pp6-7_Circular_Fiscal_TS_ES_Claude.md` | `a4d541c9-745a-49cf-a112-30df39749313.jpg` (180°) | **`INDEPENDENT_QA_PASS_FULL`** | 0 błędów; odczyt `alcootando` dosłowny z druku; mocne przesłanki wizualne i chronologiczne za przynależnością do `BOL-1956-02` (s. 6–7). |

---

## Szczegółowe wyniki weryfikacji (1–6)

### 1. `DGS-1546_Circular_DGS_1546_playas_ES_Claude.md`
- **Werdykt:** **`INDEPENDENT_QA_PASS_FULL`**
- **Zweryfikowane elementy (Ej. A):**
  - Nagłówek drukowany: `MINISTERIO DE JUSTICIA / PATRONATO DE PROTECCION A LA MUJER` + adres `Núñez de Balboa, 33` (na druku wersalikami `NUÑEZ DE BALBOA, 33`, w pliku Claude `Nuñez de Balboa, 33` — kosmetyka).
  - Tytuł okólnika: `CIRCULAR NUMERO 1.546, ANTES CITADA , / DE LA DIRECCION GENERAL DE SEGURIDAD` — zgodny znak w znak.
  - 5 norm (`Primera`–`Quinta`): pełna ciągłość i wierność wobec maszynopisu Ej. A, włącznie z osobliwościami oryginału (`bailos [sic]` w *Cuarta*, brak akcentów `prohibe`/`exceptua`, interpunkcja w *Segunda*).
  - Kwota kary w normie *Quinta*: **`500 pesetas`** + areszt zastępczy i ewentualne zamknięcie zakładów kąpielowych — potwierdzone.
  - Klauzula końcowa `ES COPIA` — potwierdzona.
  - **Brak daty na kopii:** potwierdzono niezależnie na obu fotografiach (Ej. A i Ej. B), że na samej kopii DGS-1546 **nie ma żadnej daty**. Ustalenie Claude co do rozbieżności między katalogiem (`15.06.1942`) a przywołaniem w Okólniku nr 16 Patronatu (`18.06.1942`) jest w pełni trafne i wymaga adnotacji w katalogu.
- **Uwaga porównawcza do Ej. B (`1TOfueHnMA71l_6Ss9B5e5ugjAPihe-mX.jpg`):**
  - Egzemplarz B jest inną, słabiej odbitą kopią maszynową z drobnymi wariantami formalnymi: tytuł bez kropki w numerze i z `.-` na końcu (`1546`, `SEGURIDAD.-`), brak `ES COPIA`, w *Cuarta* `bailes en trajes de baño`, a w *Quinta* kwota zapisana słownie (`quinientas pesetas`). Claude uczciwie zadeklarował, że podstawą transkrypcji jest ostrzejszy Ej. A.

---

### 2. `GR-PRINT-1943_pagina_agosto_38fdd7b0_ES_Claude.md`
- **Werdykt:** **`INDEPENDENT_QA_PASS_FULL`**
- **Zweryfikowane elementy:**
  - Początek strony: środek zasady *Tercera* (egzamin ustny a–c: Ripalda/Astete, Anatomía/Fisiología/Higiene, Leyes de protección a la familia; egzamin pisemny a–b: redakcja listu/dokumentu, arytmetyka) — 100% zgodności.
  - Zasady **`Cuarta`–`Séptima`**: wszystkie akapity kompletne, bez opuszczeń.
  - Adres w zasadzie *Cuarta*: **`Núñez de Balboa, 31`** — potwierdzony z 100% ostrością (jednoznacznie odróżnia ten druk z 1943 r. od późniejszej siedziby przy nr 33 / konwokacji z 1944 r.).
  - Daty i podpisy:
    - drukowana data konwokacji: **`Madrid, 7 de agosto de 1943`** (podpisy: `ALBERTO MARTÍN ARTAJO`, `JOSÉ MARÍA SÁNCHEZ DE MUNIAÍN`) — potwierdzone;
    - maszynopisowa data pisma przewodniego: **`Madrid, 16 de agosto de 1943`** (`EL VICEPRESIDENTE, A. Martín Artajo.`) — potwierdzone.
  - **1 niepewny odczyt wskazany przez Claude (l. 26 / l. 52):** `constituído` vs `constituido`. W dużym powiększeniu nad `i` widać lekko skośny/wydłużony znak przypominający akcent (zgodny z ortografią hiszpańską sprzed reformy RAE z 1959 r.). Oznaczenie przez Claude jako `constituído` z notą o niepewności jest wzorowe.

---

### 3. `BOL-1963-05_pp4-10_Convenio_ONU_y_Reforma_CP_ES_Claude.md` (PRIORYTET)
- **Werdykt:** **`INDEPENDENT_QA_PASS_FULL`** *(z 1 drobną literówką redakcyjną w l. 257 do skorygowania przy integracji; 0 błędów merytorycznych, liczbowych, datowych i strukturalnych)*
- **Zweryfikowana struktura i ciągłość Konwencji ONZ z 21.03.1950 (s. 4–8):**
  - Nagłówki i **Preambuła** (4 dawne instrumenty międzynarodowe z dokładnymi datami: `18 de mayo de 1904` / protokół `3 de diciembre de 1948`; `4 de mayo de 1910`; `30 de septiembre de 1921` / protokół `20 de octubre de 1947`; `11 de octubre de 1933`; projekt Ligi Narodów z `1937`) — 100% zgodności.
  - **Wszystkie artykuły `1.º`–`28`** + **Protokół końcowy** (`PROTOCOLO FINAL`, odesłanie do art. `23 a 26`): sprawdzono przejścia między kolumnami i stronami (s. 4→5 po art. 3; s. 5→6 w art. 13 pkt 3 `documen- / tos`; s. 6→7 w art. 17 pkt 4 `prima / facie`; s. 7→8 w art. 24 `rati- / ficación`). Brak pominiętych akapitów i zmyślonych słów.
  - Wiernie zachowane błędy samego druku w *Boletínie* (m.in. `participación internacional` w art. 4 [zamiast *intencional*], `que no subordine` w art. 8, `en un servicio` w art. 14, brak spójnika `y` w art. 18, `infrasquitos` i `Lake Succes` przed Protokołem końcowym).
- **Weryfikacja cyfra po cyfrze listy państw i dat na s. 8:**
  - Data złożenia dokumentu przystąpienia Hiszpanii: **`18 de junio`** (1962), wejście w życie: **`16 de septiembre de 1962`**, data noty końcowej: **`Madrid, 18 de septiembre de 1962`** — potwierdzone.
  - **Wszystkie 29 państw** (od *Albania, 6 de noviembre de 1958 (a)* po *Guinea, 26 de abril de 1962 (a)*): zweryfikowano każde państwo, każdą datę (dzień, miesiąc, rok), wszystkie adnotacje o zastrzeżeniach/deklaracjach oraz oznaczenia `(a)`/`(r)` — **29/29 bezbłędnie (0 błędów)**.
- **Weryfikacja reformy Kodeksu karnego na s. 9–10:**
  - Daty w nocie wstępnej: Ley de Bases z `23 de diciembre de 1961` (art. `3.º`, Base `9.ª`), zatwierdzenie przez Radę Ministrów `21 de diciembre` (1962) — potwierdzone.
  - Numery artykułów, kwoty grzywien i progi wiekowe:
    - `Art. 431` (w wprowadzeniu druk ma błędnie `431 y 32 [sic]`): *arresto mayor*, grzywna **`5.000 a 25.000 pesetas`**, *inhabilitación especial*; zaostrzenie dla pokrzywdzonego poniżej **`veintiún años`** — potwierdzone.
    - `Art. 432`: grzywna **`5.000 a 50.000 pesetas`** — potwierdzone.
    - `Art. 452 bis. a)` (pkt `1.º`–`3.º`): *prisión menor* w stopniu minimalnym, grzywna **`5.000 a 25.000 pesetas`**, próg `mayor de veintitrés años` — potwierdzone.
    - `Art. 452 bis. b)` (pkt `1.º`–`4.º`, przejście s. 9→10 `pre- / texto`): *prisión menor* w stopniach średnim i maksymalnym, grzywna **`5.000 a 25.000 pesetas`**, próg `menores de veintitrés años` — potwierdzone.
    - `Art. 452 bis. c)`: odesłanie do `artículo 452 bis. b)` oraz `artículo 6.º, núm. 2.º` Ley de Vagos y Maleantes — potwierdzone.
    - `Art. 452 bis. d)` (pkt `1.º`–`3.º`): *prisión menor*, grzywna **`10.000 a 100.000 pesetas`**, zamknięcie lokalu — potwierdzone.
    - `Art. 452 bis. e)`: *arresto mayor* — potwierdzone.
    - `Art. 452 bis. f)`: odesłanie do `núm. 15 del artículo 10` — potwierdzone.
    - `Art. 452 bis. g)` (*Capítulo VIII*): odesłanie do `artículos 445 y 446`, zastąpienie `artículo 432` i nowa redakcja `433` — potwierdzone.
    - `Art. 566` (Apartados `4.º`, `5.º`, z drukowanym `ofendieron [sic]`), `Art. 567` (Apartado `3.º`), uchylenie `apartado 2.º del artículo 577` — wszystko potwierdzone.
- **Wykryty drobny błąd (1 szt., niemieszczący się w kategorii błędu merytorycznego):**
  - **Linia 257** (s. 9, *Segundo.*): jest `que comprende de los nuevos artículos` → w oryginale (złamanie `compren- / de`) jest **`que comprende los nuevos artículos`** (nadmiarowe słowo `de`). Zalecana 1-wyrazowa poprawka przy integracji.
  - *(Kosmetyka ortograficzna: l. 275 `aun` wobec drukowanego `aún` — bez znaczenia merytorycznego.)*

---

### 4. `BOL-OCHOANOS_pp6-7_Circular_Fiscalia_TS_1963-04-03_ES_Claude.md`
- **Werdykt:** **`INDEPENDENT_QA_PASS_FULL`**
- **Zweryfikowane elementy:**
  - Wygięta karta (zwłaszcza s. 6): sprawdzono każdą linię obu stron — **0 przeskoków linii i 0 opuszczeń**; przeniesienie wyrazu między s. 6 a s. 7 (`especí- / fica`) w pełni poprawne.
  - Data okólnika: **`Madrid, 3 de abril de 1963`** — potwierdzona.
  - Wszystkie przywołane akty, daty i artykuły: `Decreto-ley de 3 de marzo de 1956`, Circular z `31 de enero de 1924`, `Decreto de 24 de enero` (1963), `Ley de 23 de diciembre` (1962), `Código de 1944`, art. `431` (núm. `2.º`, `4.º`, reformowany art. `431` akapit 2), `438` (núm. `1.º`), `439`, `452 bis` (apartados `a)` pkt `1.º` i `3.º`, `b)` akapit `1.º`, `c)`, `d)`), `artículo 2.º, número 2.º` Ley de Vagos y Maleantes oraz `artículo 1.º` jej Reglamento — 100% zgodności.
  - **Ramka na dole s. 7 (cytat z Piusa XII):** uczciwie opisana w l. 52 (podano autora, źródło *Discurso a las As. de Protección a la Joven*, krótki incipit i jednozdaniowe streszczenie oraz adnotację o ochronie prawnoautorskiej) **bez pełnej transkrypcji** (~120-słownego cytatu).

---

### 5. `BOL-1956-01_pp6-7_Orden_fin_y_Circular_47_ES_Claude.md`
- **Werdykt QA transkrypcji:** **`INDEPENDENT_QA_PASS_FULL`**
- **Zweryfikowane elementy:**
  - Ciągłość s. 5→6 (końcówka pkt 10 Orden z `23 de abril de 1956`: `mente al Organo competente...`), pkt `11`, data i podpis **`Madrid, 23 de abril de 1956.—Carrero.`** — potwierdzone. *(Drobna obserwacja drukarska w pkt 11, l. 18: druk ma ubytek czcionki `l` i czyta się `a colaboración`, co Claude wiernie oddał; to ten sam defekt czcionki co `procurándo'es`, `só'o`, `responsabi'idad` odnotowany przez Claude w notach.)*
  - Pełna *Circular de la Junta Nacional número 47* (pkt `1.º`–`6.º`, w tym *Vigilancia tutelar* i *Internamiento*): zweryfikowano wszystkie daty i artykuły (`BOE de 26 de abril`, `Decreto-ley de 3 de marzo`, termin `3 de junio`, art. `4.º`, `5.º`, `7.º`, `10` Orden, `Ley de 20 de diciembre de 1952`) oraz zachowane błędy druku (`procedenica`, `constacto`, `prostíbuloss`) — 100% zgodności.
- **KLUCZOWY WERDYKT #5 — KOMPLETNOŚĆ `BOL-1956-01`: `COMPLETE` (100% PEWNOŚCI)**
  - **Dowód wizualny 1 (zakończenie tekstu na s. 7):** W prawej kolumnie s. 7 tekst *Circular n.º 47* zamyka się pełnym, gramatycznie skończonym zdaniem konkludującym z kropką (`...en provecho del bien común y en prestigio de nuestra Obra.`), poniżej którego pozostaje ok. 1/3 strony całkowicie pustego białego pola (z odręczną czarną parafką/pętlą). Tekst nigdzie się nie urywa.
  - **Dowód wizualny 2 (przebicie tylnej okładki na odwrocie s. 7):** W powiększeniu dolnej połowy s. 7 (`dba54c80-d1e6-43a6-99c2-f8d9c9facf62.jpg`) przez papier wyraźnie prześwituje w odbiciu lustrzanym **tylna okładka (contracubierta = s. [8])**: ramka z napisami `REDACCIÓN Y ADMINISTRACIÓN`, `Ministerio de Justicia: Sección de Publicaciones`, `PRECIOS DE SUSCRIPCIÓN` (tabela cen prenumeraty: `125 pesetas`, `70`, `5`, `7`, `180`, `225`) oraz u samego dołu drobna stopka drukarska.
  - **Dowód strukturalny 3 (*Sumario* na s. [2]):** Sprawdzony w `BOL-1956-01_Boletin_Num_1_1956-05-05_ES_Claude.md` spis treści (*Sumario* na s. [2]) wymienia **wyłącznie trzy pozycje**: Decreto-ley (s. 3), Orden (s. 4) oraz Circular n.º 47 (s. 6).
  - **Konkluzja:** Cały numer 1 to 8-stronicowa broszura (s. [1] okładka, s. [2] Sumario, s. [3]–7 tekst merytoryczny, s. [8] tylna okładka wydawnicza). **Całą jednostkę `BOL-1956-01` należy oznaczyć jako `COMPLETE` (7/7 stron tekstowych).**

---

### 6. `a4d541c9_Boletin_1956_pp6-7_Circular_Fiscal_TS_ES_Claude.md`
- **Werdykt:** **`INDEPENDENT_QA_PASS_FULL`**
- **Zweryfikowane elementy:**
  - Zakończenie poprzedniego pisma na górze s. 6: **`Madrid, 21 de junio de 1956.—El Presidente Jefe de los Servicios.`** — potwierdzone.
  - Nagłówek: **`Circular del excelentísimo señor Fiscal del Tribunal Supremo, sobre el Decreto-ley de 3 de marzo de 1956.`** — potwierdzony.
  - Wszystkie daty i powołania prawne: `Decreto-ley de 3 de marzo` (art. `1.º`, `3.º`), `Decreto de 28 de junio de 1935`, Circular Fiscalía z `31 de enero de 1924`, Convenio z `31 de enero de 1910`, `Ley IV, título VI` i `Ley I título XXIII de la Séptima Partida`, `Orden de 23 de abril`, `artículo 237`, `artículo 431` (núm. `1.º`), `artículo 446` KK, `artículo 2.º` (núm. `2.º`) Ley de Vagos y Maleantes oraz `artículo 1.º` apartados `A)` i `G)` jej Reglamento — 100% zgodności.
  - **1 niepewny odczyt wskazany przez Claude (l. 45 / l. 64):** **`alcootando`** (w cytacie z *Siete Partidas*). W powiększeniu s. 7 wyraz drukowany jest wyraźnie jako `alcootando` (archaiczna/drukarska forma od *alcohotando* / *alcahuetando*). Zapis Claude jest w 100% wierny oryginałowi.
  - **Dopasowanie do `BOL-1956-02` (5 lipca 1956):**
    - Zgodność typografii, układu dwukolumnowego i numeracji stron (`— 6 —`, `— 7 —`) z serią *Boletín de Información* z 1956 r.
    - Przebicie tej samej tylnej okładki (`REDACCIÓN Y ADMINISTRACIÓN / PRECIOS DE SUSCRIPCIÓN`) na odwrocie s. 7 — dowodzi, że jest to ostatnia rozkładówka numeru (s. 6–7 z 8-stronicowej broszury).
    - Chronologia (`21 de junio de 1956` tuż przed wydaniem n.º 2 z `5 julio 1956`) i luka w katalogu (`BOL-1956-02` ma obecnie dokładnie 5 stron = s. 1–5) bardzo mocno potwierdzają hipotezę, że `a4d541c9` to brakujące s. 6–7 numeru `BOL-1956-02`. *(Do 100% zamknięcia połączenia wystarczy sprawdzić ostatnie słowo s. 5 w `BOL-1956-02` [`3ced7f2b`], czy kończy się sylabą `...rela-` przed `cione con el cumplimiento del Decreto-ley.`.)*
