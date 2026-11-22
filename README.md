# Archivo documental del Patronato de Protección a la Mujer

**Biblioteca digital · Digital Archive (Staging v8.1)**

Interactive documentary archive and research guide presenting digitised historical photographs, faithful **Spanish-only (ES)** transcriptions, separated source/transcription completeness and independent QA metadata, and links to related archival holdings in Spain concerning the *Patronato de Protección a la Mujer*.

## Contents (Master Catalog v8.1 — 22 November 2026)

- **`index.html`** — Standalone digital library application:
  - **Documents:** **115 public documentary units** derived from **Master Catalog v8.1** (**116 total unique units** reconciling all 232 archive JPG photographs; **1 privacy-restricted medical unit** `TOLEDO-NAMED-1966` is strictly excluded from the library).
  - **Transcriptions (Spanish-only ES):**
    - **89** complete ES transcriptions (`source_completeness: COMPLETE`, `transcription_completeness: COMPLETE`)
    - **19** incomplete ES transcriptions (partial surviving pages or missing archive scans)
    - **3** partial API-blocked multi-page publications (`BOL-1963-05`, `BOL-ISSUE-OCHOANOS-UNKNOWN`, `BOL-1956-01`)
    - **4** full API-blocked documents/spreads (`DGS-1546`, `GR-PRINT-1943-AUG`, `PRINT-UNKW-INSTITUTION-04-10`, `BOL-1956-02-SPREAD-A4D541C9`)
    - **7** units carry `claude_recovery_slot: PENDING_CLAUDE_BLOCK_RECOVERY` for seamless plug-in integration of independent Claude block recoveries.
  - **QA transparency:** Every card separates **source completeness**, **transcription completeness**, and **QA status** (`INDEPENDENT_QA_PASS_FULL`, `QA_SPOT_CHECKED`, `QA_LINKS_ONLY`, `SELF_CHECKED`, `BLOCKED_API_VERIFIED`), with direct links to original Drive JPGs, canonical ES transcriptions, and independent QA evidence reports.
  - **Other archives:** Guide to 10 related archival collections across Spain with institutional links and thematic cross-references.
  - **Master Catalog v8.1 (CSV):** https://drive.google.com/file/d/1zPUNoi5YMd7DWUR3qz4HDmlZr_YSm_RD/view

## Live vs. Staging Edition

- **Production (`main`, untouched):** https://lexisroots.github.io/Patronato-Digital-Archive/
- **Staging test branch (`staging/almu-library-v8-closure`):** https://github.com/LexisRoots/Patronato-Digital-Archive/tree/staging/almu-library-v8-closure
