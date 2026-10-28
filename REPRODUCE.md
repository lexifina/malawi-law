# How this repository was made (Malawi)

This file is written by the build on 2026-10-28, the day the source data was retrieved. Everything below is enough to rebuild this repository hash for hash.

## Sources

| Source | Address | Retrieved | Requests | Licence |
| --- | --- | --- | ---: | --- |
| MalawiLII (hosted by the Gender and Justice Unit, on the Laws.Africa Peachjam platform) | <https://malawilii.org> | 2026-10-28 | 51 | CC BY-NC 4.0, crediting MalawiLII as the source (https://malawilii.org/terms-of-use/) |
| Internet Archive Wayback Machine | <https://web.archive.org> | 2026-10-28 | None | Archived copies of MalawiLII pages; the content licence is MalawiLII's |
| Common Crawl | <https://commoncrawl.org> | 2026-10-28 | None | Common Crawl terms of use (https://commoncrawl.org/terms-of-use); the content licence is MalawiLII's |

Every response is cached by the sha256 of its URL, and the table above lists every source with its retrieval date. Lexifina keeps its fetch scripts privately; `tools/parse.py` reads only the cache and writes `corpus.json`, so the same cache always gives the same corpus.

## What is in it

| Act | Title | Versions | Span |
| --- | --- | ---: | --- |
| `constitution` | Republic of Malawi (Constitution) Act | 2 | 2017-12-31 to 2020-11-03 |
| `electoral-commission` | Electoral Commission Act | 2 | 2014-12-31 to 2018-11-02 |
| `elections` | Presidential, Parliamentary and Local Government Elections Act, 2023 | 1 | 2025-09-05 to 2025-09-05 |

The build made 5 commits:

| Commits | Kind |
| ---: | --- |
| 3 | first version of an act |
| 2 | one law on its in-force day |
| 0 | changes no amendment note explains, credited to the publisher |

Other counts:
- 0 commits on the branch `future`: laws not yet in force on 2026-10-28.
- 0 commits dated 1 January 1970: in force before 1970, with the real day in their `In-force` trailer.
- 3 laws in the record.
- 7 tags.

## Dates

Each commit is dated at noon (Africa/Blantyre) on the day the change took effect. The other dates, enacted and published, are trailers.

When a law gives no date of its own, the default rule applies: Not applied: every version is dated by MalawiLII's own expression date, the day the amendment it incorporates took effect as Laws.Africa records it (for a consolidation, the date the revised edition is as at). No date is computed from a default rule. https://malawilii.org/legislation/

## Commands, in order

```sh
# fill the cache from the sources listed above (network; Lexifina's fetch scripts are kept privately)
python -X utf8 tools/parse.py                  # cache -> corpus.json (no network)
python -X utf8 tools/build.py <folder> --repo <empty folder> --docs-date 2026-10-28
python -X utf8 tools/check_repo.py <repo> --corpus <folder>/corpus.json --write
python -X utf8 tools/build.py <folder> --repo <another empty folder> --docs-date 2026-10-28 --compare <repo>
```

In the main Lexifina repository these files live as follows:
- `fetch.py`, `parse.py` and `repo/`: in `scripts/malawi-law/`.
- `build.py`, `check_repo.py` (`check.py` there) and `on.py`: in `scripts/gitlaw_common/`, with the corpus format in `SCHEMA.md`.

## Exact inputs

- `corpus.json` sha256 `7ab9361e1160e3fdea59e665b94b5fe325c92ed73bbb2ad5208de0b76d7a31d9` (396652 bytes)
- Script blob hashes (`git hash-object`):

| Script | Blob |
| --- | --- |
| build.py | `833a2433a3ea96fd87477ccc7a2ed47dc9e24b48` |
| check.py | `426d4cfb32ce103715be6a00865c0a7bca81a56a` |
| on.py | `644a6c0857fbcc72562032b58d57aa113fee0641` |
| fetch.py | `013ff2f8eb3537df62f6bdc27da6a3755eaab305` |
| parse.py | `e3db392b2ec050c0817894287667df31b0a269b4` |

- Tools:
  - Python 3.14.0
  - git version 2.52.0.windows.1
  - curl 8.21.0 (Windows) libcurl/8.21.0 Schannel zlib/1.3.2 WinIDN WinLDAP

## Checks

Not yet run for this build.

Not yet run for this build.

These results are from the check run on the build before this one, from the same corpus.

## Decisions made by hand

- Acts were chosen by what the archives hold. The Constitution (MalawiLII lists 2 expressions: 2017-12-31 and 2020-11-03) and the Electoral Commission Act (2 expressions: 2014-12-31 and 2018-11-02) have an archived copy, with its text, of every expression MalawiLII lists, so each version is read from its own dated expression.
- The Presidential, Parliamentary and Local Government Elections Act 2023 is included from its 2025-09-05 expression only: the archived copies of its original expression of 2023-02-21 (the act as published in the Gazette) show only the source PDF, without the Akoma Ntoso text, and no OCR is used, so the act as enacted is not in this history; the first commit is the oldest version archived, naming the amending Act of 2025.
- Not taken: the Land Act 2016 (MalawiLII's current expression, 2022-07-01, after the Land (Amendment) Act 2022, is not archived), the Courts Act (its 2026-02-20 expression, after the Courts (Schedule) (Replacement) Notice 2026, is not archived), and the Penal Code and Employment Act (only their 2014-12-31 expression is archived; the Internet Archive was throttling this machine and their later expressions were not surveyed).
- The Constitution's 2014-12-31 expression (a consolidation as at 31 December 2014, from MalawiLII's earlier site, archived with its text on 2022-02-17) is left out: MalawiLII no longer lists it, and the shared adapter would date it as the act as enacted (ISSUES-malawi.md #3). The history starts at the 2017-12-31 consolidation (Fifth Revised Edition of the Laws of Malawi, L.R.O. 1/2018).
- The amending Acts' own MalawiLII pages (Act 32 of 2018, Act 13 of 2020, Act 32 of 2025) have no archived copy with their text, so their assent and Gazette dates are not given; their titles and the dates their changes took effect come from the amended act's own History and amendment list.
- Government gazettes were not used: MalawiLII's gazette pages are disallowed by its robots.txt and outside this build, and every date used here is stated by MalawiLII's expression pages. No OCR was used.
- Archives: every copy was read from the Internet Archive (raw id_ form) through scripts/gitlaw_common/wayback.py, at the machine-wide adaptive rate; Common Crawl's index (index.commoncrawl.org) timed out from this machine during the retrieval (2026-10-28, 21:55 to 23:10 UTC), so no Common Crawl copy is used, though lii.py tries it first.
- The current-expression check reads MalawiLII's own legislation listing in its newest archived copies (listing.py, listing_check.json): for all three acts the listing names the expression this history ends with.
- Licence and terms: MalawiLII (hosted by the Gender and Justice Unit) licenses primary and secondary law content CC BY-NC 4.0, crediting MalawiLII as the source, and its terms say "Scraping and bulk downloading from this website is strictly prohibited"; its robots.txt sends Content-Signal ai-train=no, ai-input=no and Crawl-delay 5. No MalawiLII page was fetched: every page was read from archived copies, for the configured acts only. The user decided on 2026-10-28 that reading these archived copies is acceptable (relayed by the coordinator: "scraping wayback is fair game, dont overdo it"). The repository stays private; CC BY-NC allows only non-commercial use. No legal text was given to a model.
- Version dates are MalawiLII's expression dates. Laws.Africa's terminology guide (https://docs.laws.africa/getting-started/terminology-guide) says "Amendments to Principal works come into force on the Commencement date of the Amending work" and that the first point in time is "the work as originally published"; so an amendment's expression is dated by its commencement (in force), and an act's original expression by its publication, which is replaced by the commencement date the page states.
- Credits: a version whose History names exactly one amending law (and no consolidation) between it and the previous version is credited to that law for every provision that changed. Otherwise a provision is credited only to laws that MalawiLII's editorial note inside that provision links to; the rest are unexplained (publisher).
- Editorial notes (akn-remark) are left out of the text and used only as credit evidence, except where a provision has no other text (repealed or spent), where the note is the provision's whole printed content.
- Part, Chapter and Division headings are left out; each provision file starts with its own number and heading. Every other text of each version is in a provision file: parse.py checks this per version (verification.json, fidelity).
- PPLGE Act 2023: the LII lists expression(s) 2023-02-21, but neither Common Crawl nor the Internet Archive holds a copy with its text, so their changes appear in the next version that is archived.

## What AI did and did not do

The fetch, parse and check scripts were written by Claude Code running Claude Opus 5.5 (`claude-opus-5-5`) under Lexifina's direction.

No model wrote, translated or corrected legal text. No model runs at build time. Every word of law in this repository comes from the official sources above, through code that anyone can rerun.

The commit messages are written by `build.py` from the source data.

Model use at data-build time:
- Claude Code (Claude Opus 5.5, claude-opus-5-5) wrote the configuration and the Malawi-specific scripts, and chose the acts. No model wrote, summarised or transformed legal text: parse.py is deterministic code.
