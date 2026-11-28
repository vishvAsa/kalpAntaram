+++
title = "+History OD"
+++
<details><summary>LLM proofreading state</summary>

- **Source PDFs**: `/media/vvasuki/vData/text/granthasangrahaH/kalpaH/kANe/v{1p1,1p2,2p1,2p2,3,4,5p1,5p2}.pdf` (render individual pages at 400 dpi with `pdftoppm`; never run CPU-heavy local Tesseract OCR).
- **Second-witness text**: `indike.org` (`https://indike.org/pramana/ins.polity.kane-1930`, mirrorable via `doc_curation_projects/sites/pramana_sync.py`) recovers ~95-98% of 8pt Devanagari and de-columnizes two-column indices, but drops `[[P...]]` page markers, smooths typos, and occasionally drops visarga/subscript-ra or memorizes śāstra phrases — always verify against the 400 dpi PDF scans and preserve `[[RAW_OCR|NEW]]` diffs.
- **Status by volume**:
  - `v5p1/`, `v5p2/`: Main targets & `_index.md` files completed (`"Gemini 4 Hydrogen"`: `v5p1/18` + `0/Publishers_Note.md`; `v5p2/24, 34, 35`, `11/word-Index.md`, `00/*`, `11/Epilogue.md` asterisk fix). Only pre-existing `odd_asterisk_paragraphs` (unescaped `*` inside `[[OLD|...]]` + minor italics in `v5p1/09,10` & `v5p2/20-23,25-33`) and printed `<u>` emphasis tags (`v5p1/01-03,11-12,14,16-19`, `v5p2/36,37`) remain in older files.
  - `v4/`, `v3/`: Body chapters proofread (`v4` + `0/Table_of_Contents.md`, `v3`); `audit_proofread_dir` shows 0 missing/orphan fn defs, 0 duplicate pages, and 0 unclosed/nested brackets. Remaining: raw `v4/0/Additions_and_Corrections.md`, `<u>` tags (`v4/07-10`), `[[??]]` (`v4/03`), odd asterisks, and volume `_index.md` title-page OCR.
  - `v1p1/`, `v1p2/`, `v2p1/`, `v2p2/`: Most body chapters proofread (plus `v1p1/00/list_of_abbreviations.md`, `v1p2/000/{Table_of_Contents,Preface,Corrections_and_Additions}.md` by `"Gemini 4 Hydrogen"`); pending unproofread front/back matter (`v1p2/000/{General_Index,Synopsis_of_Contents}` + `Dharmasastra_Works_and_Writers/*`, `v2p1/00/*`, `v2p2/36/*`), stray raw pockets (`v1p1/50_yama` pp. 526-528, `v1p1/61_vishvarUpa` L49-61), verification of unbracketed (`edits==0`) chapters (`v1p1`, `v1p2`, `v2p1/13`, `v2p2`), and odd asterisks / title-page `_index.md` cleanups. (Note `indike.org` `v1.c6` reflects the 1930 1st ed. chapter layout whereas `v1p1`/`v1p2` are 2nd revised ed., though `v1.c8` Appendix A aligns.)
- **Key lessons**: Preserve `##` headings and original prose; mark genuinely illegible 8pt spans as `...[[??]]` (never guess); intentionally empty-half `[[|NEW]]` / `[[OLD|]]` edits are valid, but avoid `[[X|X]]`, `[[|]]`, unclosed `[[`, or nesting `[[`/`[^` inside `[[...|...]]`; remove `(Continued from last page)` headers; define footnotes cleanly after the referencing paragraph (`[^N]: ...`).
</details>

Source: [sanatana hyperlinked](https://sanatana.in/dharmashastra/Volumes) ,  
Source: [TW](https://archive.org/details/kANe_history_of_dharmashAstra-s/)  
other copies [all](https://archive.org/search?query=kAne+dharmasastra)
