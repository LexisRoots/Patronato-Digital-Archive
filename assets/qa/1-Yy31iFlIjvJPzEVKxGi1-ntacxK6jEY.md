# Raport Dowodowy Niezależnego QA — Stream B1 (`BOL-1963-05`, `BOL-1963-06`, `BOL-1963-08`)

**Data weryfikacji:** 2026-11-21  
**Rola:** Niezależny Agent QA (Stream B1)  
**Metodologia:**
1. Programowa weryfikacja 100% linków Google Drive (wszystkie 22 źródłowe JPG w trzech biuletynach + 1 odwołanie krzyżowe) przeciwko `/home/antigravity/patronato_final/MASTER_CATALOG_PATRONATO_ALMU_v7.json` oraz `/home/antigravity/patronato_closure/jpg_manifest.json`.
2. Bezpośrednia, niezależna weryfikacja wizualna przeciwko oryginalnym fotografiom JPG z `/home/antigravity/patronato_closure/upright/` (obróconym o 180° w PIL i rozdzielonym na pojedyncze strony dla tabel oraz drobnego druku).
3. Uczciwe nadanie statusu QA: ponieważ biuletyny są wielostronicowe i zostały zweryfikowane rygorystycznie w trybie wyrywkowym (z pełną weryfikacją słowo-po-słowie / cyfra-po-cyfrze stron kluczowych, tabel statystycznych, nagłówków, *Sumario* i stron krzyżowych), wszystkie trzy publikacje otrzymują uczciwy status **`QA_SPOT_CHECKED`**.

---

## 1. Tabela werdyktów QA (Stream B1)

| # | Doc ID | Plik w `/home/antigravity/patronato_closure/stream_b/` | Zakres JPG / Strony | Werdykt QA | Podsumowanie ustaleń |
|---|---|---|---|---|---|
| 1 | `BOL-1963-05` | `BOL-1963-05_Boletin_Num_5_1963-01-15_ES.md` | 10 JPG własnych + 1 cross-ref (JPG 1 z `BOL-1963-06` dla s. 20); 20/20 s. (`COMPLETE` fizycznie, `PARTIAL_API_BLOCK` dla s. 4–10) | **`QA_SPOT_CHECKED`** | 100% linków Drive zgodnych z v7 i manifestem; prawidłowe przestawienie odwróconych JPG 9 (s. 14–15) i JPG 8 (s. 16–17); rzetelna dokumentacja blokady API na s. 4–10 bez halucynacji; s. 20 z JPG 1 `BOL-1963-06` potwierdzona. **Naprawiono 1 literówkę na s. 19** (`Regenteado` → `Regentado`) i zaktualizowano `Estado de QA`. |
| 2 | `BOL-1963-06` | `BOL-1963-06_Boletin_Num_6_1963-04-15_ES.md` | 7 JPG; 13/16 s. (`INCOMPLETE`, brak s. 14–16; `COMPLETE_OF_AVAILABLE`) | **`QA_SPOT_CHECKED`** | 100% linków Drive zgodnych z v7 i manifestem; prawidłowe przestawienie JPG 6 (s. 6–7) przed JPG 4–5 (s. 8–11); wykaz brakujących s. 14–16 zgodny z *Sumario*; **tabele statystyczne s. 9–10 zweryfikowane 100% cyfra po cyfrze — 0 błędów liczbowych**. Zaktualizowano `Estado de QA`. |
| 3 | `BOL-1963-08` | `BOL-1963-08_Boletin_Num_8_1963-10-15_ES.md` | 5 JPG; 9/24 s. + s. 16 adjunta z núm. 7 (`INCOMPLETE`, brak s. 4–17 i s. 24; `COMPLETE_OF_AVAILABLE`) | **`QA_SPOT_CHECKED`** | 100% linków Drive zgodnych z v7 i manifestem; wykaz brakujących 15 stron (4–17, 24) zgodny z *Sumario*; s. 16 adjunta z núm. 7 zweryfikowana słowo po słowie; **tabele statystyczne s. 18 zweryfikowane 100% cyfra po cyfrze — 0 błędów**. Zaktualizowano `Estado de QA`. |

---

## 2. Programowa weryfikacja linków Drive JPG (vs `MASTER_CATALOG_PATRONATO_ALMU_v7.json` i `jpg_manifest.json`)

- **`BOL-1963-05` (cat. 103):** Wszystkie 10/10 Drive ID z katalogu v7 obecne w pliku `.md` i w `jpg_manifest.json` (`1cba3y1Y...`, `1eMOKmet...`, `1dIuNM6u...`, `1R0qmYJG...`, `1I1PhCRS...`, `12hNT_n1...`, `1fm31COe...`, `1mYwGFnf...`, `15yuXRNd...`, `123CVrQ4...`). Dodatkowe 11. ID (`16axVZtYFI6h39SyIjmSqtKXcAiWRK3DD`) to prawidłowa referencja krzyżowa do JPG 1 z `BOL-1963-06` (lewa połowa = s. 20 `BOL-1963-05`).
- **`BOL-1963-06` (cat. 104):** Wszystkie 7/7 Drive ID z katalogu v7 obecne w pliku `.md` i w `jpg_manifest.json` (`16axVZtY...`, `1diTMh4C...`, `1LCG4LZI...`, `1n0T4oMa...`, `12UKUtoA...`, `1PIlOKrq...`, `1koZ2YI1...`). Brak obcych/błędnych ID.
- **`BOL-1963-08` (cat. 105):** Wszystkie 5/5 Drive ID z katalogu v7 obecne w pliku `.md` i w `jpg_manifest.json` (`16Mc0jnr...`, `1LUrhw7-...`, `1ISdz1k0...`, `1HR2ERk2...`, `1PouAR1S...`). Brak obcych/błędnych ID.

---

## 3. Szczegółowe dowody weryfikacji wizualnej (obrócone JPG 180° w PIL)

### 3.1. `BOL-1963-05_Boletin_Num_5_1963-01-15_ES.md`
- **Okładka zewnętrzna + Portada s. 1 (`1cba3y1YG2Lu4pYHG9NtUxbc-PCNEMrHu.jpg`):**
  - Lewa połowa (okładka ogólna `MINISTERIO DE JUSTICIA / BOLETIN DE INFORMACION`): pełna tabela cen prenumeraty (`125 pesetas`, `70`, `6`, `7`, `180`, `225`) i stopka `GRÁFICAS UGUINA. - MADRID` — **100% zgodne**.
  - Prawa połowa (Portada s. 1): `NUM. 578`, `AÑO XVII`, `NUMERO 5`, `15 de enero de 1963`, `MADRID` — **100% zgodne**.
- **Sumario s. 2 + Propósito s. 3 (`1eMOKmetD4CTEQOUrRiB7-lNfVkQGXym0.jpg`):**
  - Wszystkie 8 pozycji *Sumario* (strony 3, 4, 9, 11, 13, 16, 18, 20) oraz stopka `GRÁFICAS UGUINA - MADRID | Depósito legal, M., Sep., 883-1958.` — **100% zgodne**.
  - Pełny tekst `PROPOSITO` na s. 3 zweryfikowany akapit po akapicie — **100% zgodny**.
- **Weryfikacja dokumentacji blokady filtra API na s. 4–10 (`1dIuNM6u...`, `1I1PhCRS...`, `12hNT_n1...`):**
  - Wizualnie potwierdzono granice i tytuły na oryginalnych JPG bez przepisywania chronionego/filtrowanego tekstu:
    - s. 4–8: *ADHESION DE ESPAÑA AL CONVENIO PARA LA REPRESION DE LA TRATA DE PERSONAS Y DE LA EXPLOTACION DE LA PROSTITUCION AJENA, FIRMADO EN LAKE SUCCESS, NUEVA YORK, EL 21 DE MARZO DE 1950* (Preámbulo, Arts. 1.º–28, Protocolo Final, nota z 18 de junio / 16 de septiembre de 1962, wykaz państw, `Madrid, 18 de septiembre de 1962`).
    - s. 9–10: *REFORMA DEL CODIGO PENAL ESPAÑOL EN LOS DELITOS CONTRA LA HONESTIDAD* (Ley de Bases 23-12-1961, Consejo de Ministros 21-12-1962, Cap. II arts. 431–432, Cap. VII arts. 452 bis a)–f), itd.).
  - **Ocena:** Dokumentacja blokady API (`PARTIAL_API_BLOCK`) jest w 100% rzetelna, precyzyjna, bez halucynacji i bez jakiegokolwiek obchodzenia filtra.
- **Komentarz M. Tallada s. 11 (`12hNT_n1N5djB94eZFOF3PZsWqPbQCKf0.jpg`, prawa połowa):** Zweryfikowano w całości słowo po słowie — **100% zgodne**.
- **Kolejność odwróconych skanów s. 14–15 i s. 16–17 (`15yuXRNd...` = JPG 9 katalogowy, `1mYwGFnf...` = JPG 8 katalogowy):**
  - Potwierdzono wizualnie, że `15yuXRNd...` zawiera `— 14 —` i `— 15 —`, natomiast `1mYwGFnf...` zawiera `CONGRESOS Y REUNIONES` (s. 16) i `— 17 —`. Reordering w pliku `.md` jest **100% poprawny**.
  - Wyrywkowa kontrola s. 15 i s. 17: wiernie zachowane nawet osobliwości oryginału (np. `decisiones adaptadas` na s. 15, `del 27 al 8 de agosto de 1963` na s. 17).
- **Noticiario s. 19 (`123CVrQ4ankO2megumagnfoXZG9ZjFKYn.jpg`, prawa połowa):**
  - Zweryfikowano słowo po słowie punkty 11–14 i Colaboradoras 1.º–4.º.
  - **Wykryty i naprawiony błąd (linia 414):** W transkrypcji było `Regenteado por Religiosas del Buen Pastor.`, podczas gdy oryginał JPG drukuje wyraźnie **`Regentado por Religiosas del Buen Pastor.`** — naprawiono bezpośrednio w pliku `.md`.
- **Strona 20 — Sección de consultas (`16axVZtYFI6h39SyIjmSqtKXcAiWRK3DD.jpg`, lewa połowa JPG 1 z `BOL-1963-06`):**
  - Na prześwicie rewersu wyraźnie widać s. 19 (`11. Hogar de la Purísima...`), co bezspornie potwierdza przynależność do `BOL-1963-05`.
  - Zweryfikowano cały tekst słowo po słowie — 100% zgodności merytorycznej. *Drobna uwaga nieblokująca:* w oryginale wydrukowano literówkę nazwiska `don Enrique Jiménez Ansejo`, którą agent B1 znormalizował do historycznie poprawnej formy `Asenjo` (linia 435).

### 3.2. `BOL-1963-06_Boletin_Num_6_1963-04-15_ES.md`
- **Portada s. 1 (`16axVZtYFI6h39SyIjmSqtKXcAiWRK3DD.jpg`, prawa połowa):** `NUM. 587`, `AÑO XVII`, `NUMERO 6`, `15 de abril de 1963`, `MADRID` — **100% zgodne**.
- **Sumario s. 2 + A nuestras Juntas s. 3 (`1diTMh4C7xwTPdqT9Js0i2qlSXz7fAnmX.jpg`):**
  - Wszystkie 6 pozycji *Sumario* (3, 5, 9, 11, 14, 16) i stopka `GRÁFICAS UGUINA - MADRID. | Depósito legal, M., Sep., 883-1958.` — **100% zgodne**.
  - Wyrywkowa weryfikacja s. 3 (*Por M. TALLADA, Secretario General del Patronato.*) — **100% zgodne**.
- **Kolejność przestawionego JPG 6 (`1PIlOKrqudnhZXOROTiv41JLU6FuH-2hw.jpg`):**
  - Wizualnie potwierdzono paginację `— 6 —` i `— 7 —`; umieszczenie przed JPG 4 (`8–9`) i JPG 5 (`10–11`) jest **100% poprawne**. Wiernie zachowano oryginalną literówkę `dependiente` (l. poj.) na s. 6.
- **Tabele statystyczne C. O. C. Madrid 1962 — s. 9 (`1n0T4oMaxKBv6_guJwJeqwi7LxCV_dna4.jpg`, prawa) i s. 10 (`12UKUtoAW3Uo9UJYeP6rCYjOBQo5DJ1mK.jpg`, lewa):**
  - Zweryfikowano **100% wszystkich wierszy i wszystkich liczb** we wszystkich 10 tabelach:
    - *Procedencias* (108, 89, 23, 1, 1, 2 = **224**), *A descontar* (28, 5 = **33**; expedientes abiertos = **191**),
    - *Edades* (3, 23, 26, 38, 24, 16, 25, 23, 8, 4, 1 = **191**),
    - *Salieron con destino a* (111, 28, 5, 4, 23, 2, 1, 2, 25, 2, 1, 13, 4, 1, 2),
    - *Causas o motivos* (9, 41, 20, 12, 5, 1, 3, 50, 13, 34, 1, 2 = **191**),
    - *Instrucción religiosa* (19, 23, 51, 84, 14 = **191**),
    - *Instrucción cultural* (16, 22, 47, 92, 14 = **191**),
    - *Profesiones* (90, 12, 13, 5, 4, 2, 14, 3, 15, 19, 14 = **191**),
    - *Escolaridad* (101, 30, 64, 26, 7, 14),
    - *Ambiente familiar* (72, 55, 9, 14, 8, 15, 4, 14 = **191**).
  - **Wynik:** **0 błędów liczbowych**. *Drobna uwaga nieblokująca:* w tabeli *Profesiones* oryginał drukuje `Servientas, asistentas`, znormalizowane w MD do `Sirvientas, asistentas` (linia 315); w tytule s. 9 pominięto przecinek po `CLASIFICACION`.
- **Końcówka s. 12–13 (`1koZ2YI19VF-lUNXRePwwk19fPQ0BT7l_.jpg`) i brakujące s. 14–16:**
  - Potwierdzono paginację `— 12 —` i `— 13 —`, zakończenie artykułu (`exigencias de su programa de tecnificación.`) oraz brak JPG dla stron 14–16 (*Noticiario*, *Sección de consultas*). Wykaz braków jest **100% dokładny**.

### 3.3. `BOL-1963-08_Boletin_Num_8_1963-10-15_ES.md`
- **Strona adjunta z núm. 7 (`16Mc0jnr4EjUXAiGIf8Su0SHjVCLTJO4d.jpg`, lewa połowa):**
  - Na prześwicie rewersu widać `— 15 —`, co bezspornie potwierdza, że to s. 16 poprzedniego numeru (Boletín núm. 7 z lipca 1963, rec. *Revue Abolitionniste* nr 200 maj–czerwiec 1963).
  - Zweryfikowano całą stronę `NOTAS BIBLIOGRAFICAS` słowo po słowie — **100% zgodne** (drobna normalizacja akcentu `Rumania` → `Rumanía`).
- **Portada s. 1 (`16Mc0jnr4EjUXAiGIf8Su0SHjVCLTJO4d.jpg`, prawa połowa):** `NUM. 605`, `AÑO XVII`, `NUMERO 8`, `15 de octubre de 1963`, `MADRID` — **100% zgodne**.
- **Sumario s. 2 + Editorial s. 3 (`1LUrhw7-MZhyVlFjtWaua_E2VKdxnllaS.jpg`):**
  - Wszystkie pozycje *Sumario* (strony 3, 6, 10, 13, 14, 17, 19, 20, 21, 22, 23, 24), ramka z mottem i `Depósito legal, M., Sep., 883-1958.` — **100% zgodne**.
  - Wykaz brakujących 15 stron (**4–17** i **24**) w pełni zgodny z *Sumario* i dostępnymi 5 JPG.
  - Editorial s. 3 (*LAS CASAS DE FAMILIA*) zweryfikowany — wiernie zachowane nawet oryginalne usterki składniowe druku (`proteger a las trabajadores`, `con las que ya veníamos desde hacía mucho tiempo, con ese mismo problema`).
- **Tabele statystyczne Cursillos F. I. P. i Resultados — s. 18 (`1ISdz1k0U00wtUcTfMwkmGIl6tDRD-few.jpg`, lewa połowa):**
  - Zweryfikowano **100% obu tabel cyfra po cyfrze i wiersz po wierszu** (9 wierszy górnej tabeli: numery nomenclátor `242, 226, 253, 218, 229`, daty, okresy, stypendia `12, 12, 12, 15, 12, 12, 15, 10, 40`; oraz 9 wierszy dolnej tabeli *RESULTADOS*: `24/8/8/0`, `7/1/1/1`, `3/2/6/1`, `8/4/2/1`, `5/3/4/0`, `11/1/—/—`, `11/1/—/—`, `10/2/—/—`, `5/6/4/—`).
  - **Wynik:** **0 błędów liczbowych ani tekstowych**; wiernie zachowane nawet literówki drukarskie oryginału (`10 maquistas punto`, `15 alfonbristas`).
- **Wyrywkowa weryfikacja s. 19, 21, 22–23 (`1ISdz1k0...` prawa, `1HR2ERk2...` prawa, `1PouAR1S...`):**
  - Potwierdzono wysoką wierność transkrypcji, łącznie z zachowaniem oryginalnych literówek drukarskich na s. 21 (`la derechos`, `Difíciles de caracteriológicos`, `circular de estudios`), s. 22 (`y social y equivalente`) i s. 23 (`programado`). Potwierdzono brak sfotografowanej s. 24 (*Bibliografía* widoczna jedynie w prześwicie rewersu s. 23).

---

## 4. Podsumowanie zmian wprowadzonych bezpośrednio przez QA

1. `/home/antigravity/patronato_closure/stream_b/BOL-1963-05_Boletin_Num_5_1963-01-15_ES.md`:
   - Poprawiono literówkę na s. 19 (linia 414): `Regenteado por Religiosas del Buen Pastor.` → `Regentado por Religiosas del Buen Pastor.`
   - Zaktualizowano `- **Estado de QA:**` z `SELF_CHECKED` na `QA_SPOT_CHECKED`.
2. `/home/antigravity/patronato_closure/stream_b/BOL-1963-06_Boletin_Num_6_1963-04-15_ES.md`:
   - Zaktualizowano `- **Estado de QA:**` z `SELF_CHECKED` na `QA_SPOT_CHECKED`.
3. `/home/antigravity/patronato_closure/stream_b/BOL-1963-08_Boletin_Num_8_1963-10-15_ES.md`:
   - Zaktualizowano `- **Estado de QA:**` z `SELF_CHECKED` na `QA_SPOT_CHECKED`.

## 5. Bilans końcowy QA (Stream B1)

- **`QA_SPOT_CHECKED`:** 3/3 publikacje (`BOL-1963-05`, `BOL-1963-06`, `BOL-1963-08`).
- **`FAIL_NEEDS_FIX`:** 0 publikacji.
