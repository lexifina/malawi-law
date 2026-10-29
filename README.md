# Malawi: law history in git

The law of Malawi as a git history: one file per provision, one commit per law on the day it took effect, and the law that made each change as the commit's author. `git blame` names the law behind every paragraph; `git log` lists every change to a provision; `tools/on.py` gives the text in force on any day.

It follows the shared design of [lexifina/global-law](https://github.com/lexifina/global-law), which places it at `mw/`. Every version is a dated point-in-time version published by [MalawiLII](https://malawilii.org) on the Laws.Africa Peachjam platform.

**What is in it now**

| Folder | Act | Versions | History |
| --- | --- | ---: | --- |
| `constitution/` | [Republic of Malawi (Constitution) Act](https://malawilii.org/akn/mw/act/1994/20) | 2 | 2017-12-31 to 2020-11-03 |
| `electoral-commission/` | [Electoral Commission Act](https://malawilii.org/akn/mw/act/1998/11) | 2 | 2014-12-31 to 2018-11-02 |
| `elections/` | [Presidential, Parliamentary and Local Government Elections Act, 2023](https://malawilii.org/akn/mw/act/2023/10) | 1 | 2025-09-05 to 2025-09-05 |
| `criminal-procedure-evidence/` | [Criminal Procedure and Evidence Code](https://malawilii.org/akn/mw/act/1967/36) | 1 | 2014-12-31 to 2014-12-31 |
| `employment/` | [Employment Act](https://malawilii.org/akn/mw/act/2000/6) | 1 | 2014-12-31 to 2014-12-31 |
| `labour-relations/` | [Labour Relations Act](https://malawilii.org/akn/mw/act/1996/16) | 1 | 2014-12-31 to 2014-12-31 |
| `corrupt-practices/` | [Corrupt Practices Act](https://malawilii.org/akn/mw/act/1995/18) | 1 | 2014-12-31 to 2014-12-31 |
| `police/` | [Police Act](https://malawilii.org/akn/mw/act/2010/12) | 1 | 2014-12-31 to 2014-12-31 |
| `child-care-protection-justice/` | [Child Care, Protection and Justice Act](https://malawilii.org/akn/mw/act/2010/22) | 1 | 2014-12-31 to 2014-12-31 |
| `deceased-estates/` | [Deceased Estates (Wills, Inheritance and Protection) Act](https://malawilii.org/akn/mw/act/2011/14) | 1 | 2014-12-31 to 2014-12-31 |
| `marriage-divorce-family-relations/` | [Marriage, Divorce and Family Relations Act](https://malawilii.org/akn/mw/act/2015/4) | 1 | 2017-12-31 to 2017-12-31 |
| `electronic-transactions-cyber-security/` | [Electronic Transactions and Cyber Security Act](https://malawilii.org/akn/mw/act/2016/33) | 1 | 2017-12-31 to 2017-12-31 |
| `insolvency/` | [Insolvency Act](https://malawilii.org/akn/mw/act/2016/9) | 1 | 2017-12-31 to 2017-12-31 |
| `access-to-information/` | [Access to Information Act, 2016](https://malawilii.org/akn/mw/act/2017/13) | 1 | 2020-09-30 to 2020-09-30 |
| `tax-administration/` | [Tax Administration Act, 2021](https://malawilii.org/akn/mw/act/2021/13) | 1 | 2025-04-01 to 2025-04-01 |
| `defence-force/` | [Defence Force Act](https://malawilii.org/akn/mw/act/2004/11) | 2 | 2014-12-31 to 2018-02-02 |
| `forestry/` | [Forestry Act](https://malawilii.org/akn/mw/act/1997/11) | 2 | 2017-12-31 to 2020-06-19 |
| `energy-regulation/` | [Energy Regulation Act](https://malawilii.org/akn/mw/act/2004/20) | 2 | 2014-12-31 to 2025-01-14 |
| `human-rights-commission/` | [Human Rights Commission Act](https://malawilii.org/akn/mw/act/1998/27) | 1 | 2017-12-31 to 2017-12-31 |
| `local-government/` | [Local Government Act](https://malawilii.org/akn/mw/act/1998/42) | 1 | 2017-12-31 to 2017-12-31 |
| `national-parks-and-wildlife/` | [National Parks and Wildlife Act](https://malawilii.org/akn/mw/act/1992/11) | 1 | 2017-12-31 to 2017-12-31 |
| `trafficking-in-persons/` | [Trafficking in Persons Act](https://malawilii.org/akn/mw/act/2015/3) | 1 | 2017-12-31 to 2017-12-31 |
| `payment-systems/` | [Payment Systems Act](https://malawilii.org/akn/mw/act/2016/15) | 1 | 2017-12-31 to 2017-12-31 |
| `copyright/` | [Copyright Act](https://malawilii.org/akn/mw/act/2016/26) | 1 | 2017-12-31 to 2017-12-31 |
| `communications/` | [Communications Act](https://malawilii.org/akn/mw/act/2016/34) | 1 | 2017-12-31 to 2017-12-31 |
| `financial-crimes/` | [Financial Crimes Act](https://malawilii.org/akn/mw/act/2017/14) | 1 | 2017-12-31 to 2017-12-31 |
| `public-procurement-and-disposal-of-public-assets/` | [Public Procurement and Disposal of Public Assets Act](https://malawilii.org/akn/mw/act/2017/27) | 1 | 2017-12-31 to 2017-12-31 |
| `hiv-and-aids-prevention-and-management/` | [HIV and AIDS (Prevention and Management) Act, 2017](https://malawilii.org/akn/mw/act/2018/9) | 1 | 2018-06-15 to 2018-06-15 |
| `revenue-appeals-tribunal/` | [Revenue Appeals Tribunal Act, 2021](https://malawilii.org/akn/mw/act/2021/14) | 1 | 2025-04-01 to 2025-04-01 |
| `property-valuation/` | [Property Valuation Act, 2024](https://malawilii.org/akn/mw/act/2024/26) | 1 | 2025-01-13 to 2025-01-13 |
| `sectional-titles/` | [Sectional Titles Act, 2024](https://malawilii.org/akn/mw/act/2024/27) | 1 | 2025-01-13 to 2025-01-13 |
| `real-estate-management/` | [Real Estate Management Act, 2024](https://malawilii.org/akn/mw/act/2024/28) | 1 | 2025-01-13 to 2025-01-13 |
| `liquid-fuels-and-gas-production-and-supply/` | [Liquid Fuels and Gas (Production and Supply) Act](https://malawilii.org/akn/mw/act/2004/23) | 2 | 2014-12-31 to 2025-01-14 |
| `land-survey/` | [Land Survey Act](https://malawilii.org/akn/mw/act/1952/14) | 1 | 2017-12-31 to 2017-12-31 |
| `lands-acquisition-and-compensation/` | [Lands Acquisition and Compensation Act](https://malawilii.org/akn/mw/act/1970/21) | 1 | 2017-12-31 to 2017-12-31 |
| `credit-reference-bureau/` | [Credit Reference Bureau Act](https://malawilii.org/akn/mw/act/2010/18) | 1 | 2017-12-31 to 2017-12-31 |

**Republic of Malawi (Constitution) Act**

| In force | Author |
| --- | --- |
| 2017-12-31 | publisher (MalawiLII): oldest version available |
| 2020-11-03 | Act 13 of 2020 |

**Electoral Commission Act**

| In force | Author |
| --- | --- |
| 2014-12-31 | publisher (MalawiLII): oldest version available |
| 2018-11-02 | Act 32 of 2018 |

**Presidential, Parliamentary and Local Government Elections Act, 2023**

| In force | Author |
| --- | --- |
| 2025-09-05 | publisher (MalawiLII): oldest version available |

Each folder's `README.md` lists every provision, how often it changed and when.

## A lawyer's questions as git commands

| Question | Command |
| --- | --- |
| What did sec-067 say on 2017-12-31? | `python tools/on.py 2017-12-31 constitution sec-067` |
| The same, with raw git (bash) | `git show $(git rev-list -1 --before="2017-12-31T23:59:59Z" main -- constitution/sec-067.md):constitution/sec-067.md` |
| The same, in PowerShell | `$r = git rev-list -1 --before="2017-12-31T23:59:59Z" main -- constitution/sec-067.md; git show "$($r):constitution/sec-067.md"` |
| Which law wrote each line? | `git blame constitution/sec-067.md` |
| Every change, word by word | `git log -p --word-diff constitution/sec-067.md` |
| Every law in the record, in order | `git log --reverse --format="%ad %an" --date=short main` |
| Everything one law changed | `git show law/<key>` (tags `law/<key>` mark each law's commit) |
| The whole act on a date | `python tools/on.py 2017-12-31 constitution` |
| Which law gave a provision its wording on a date | `python tools/on.py --law 2017-12-31 constitution sec-067` |

After a rebuild, refresh tags with `git fetch --force --tags`: a plain fetch keeps stale tags.

## Dates

- Each commit is dated at **noon, Africa/Blantyre, on the day the change took effect**. The day is also in the `In-force:` trailer, which the tools read; enactment (assent) and Gazette publication dates are trailers too, where MalawiLII states them.
- **The day is MalawiLII's.** Each version is a Laws.Africa expression, and its date is the day the amendment it takes in came into force, as the amendment list says ("[Amended by <Act> on <date>]"). For a consolidation (a revised edition) it is the date the edition is as at. An act's original expression is dated by its Gazette publication; where MalawiLII gives a later commencement date ("Commenced on ..."), the first version is dated by that instead (see REPRODUCE.md, decisions).
- `--before="YYYY-MM-DD"` alone uses your clock's time of day, so a law that took effect that day may be missed before noon. Use `T23:59:59Z` as above, or the tool.

## How it is checked

- Every version is read back from git on the day it took effect and on the day before (`tools/check_repo.py`); both must match `corpus.json`. Results are in `REPRODUCE.md`.
- **Against MalawiLII's current text:** the last version of each act is the expression MalawiLII's own legislation listing names as current, in its newest archived copies (Internet Archive captures of 2026-04-19 to 2026-06-10; all match), and is the text of that expression page.
- **Every version is its own dated expression**: each was parsed from an archived copy of exactly that expression's page, whose sha256 is recorded with the version.
- The repository is rebuilt from the same data a second time and must give identical hashes.

## What "author" means

The author of a commit is the law that made the change, with an e-mail address that cannot exist, so `git blame` and `git log --author` name laws. The committer is always Lexifina.

- **Credits come only from MalawiLII's own notes.** A version whose History entry names one amending Act is credited to it. Where one version takes in several Acts, or a revised edition, a provision is credited to an Act only if MalawiLII's editorial note in that provision names it ("[section 5 amended by section 2 of Act 3 of 2020]"); the rest are committed by the publisher and labelled "unexplained", and the commit message names the Acts the version takes in.
- **The first commit** is the act as enacted where that is the oldest version; otherwise it is the oldest version available (a consolidation), credited to the publisher.
- Blame credits whole lines (one paragraph per line). Use `git log -p --word-diff` to see exactly which words each change made.

## What it does not show

- **Only the versions MalawiLII publishes.** Changes before its oldest version are not separate commits.
- **Editorial notes.** MalawiLII's bracketed notes ("[Act No. 18 of 1996]", "[section 5 amended by ...]") are left out of the text and used only for credits, except where a provision has no other text (repealed or spent), where the note is what MalawiLII prints and is kept.
- **Headings above the provision** (Part, Chapter, Division) are left out; each file starts with its own number and heading. Footnotes are kept at the end of the file.
- **Amendments not yet applied.** Where the LII lists an amendment as not yet applied to its consolidated text, it is not in this history; REPRODUCE.md lists each one.
- **No OCR.** Acts the LII shows only as scanned PDFs are not included.

## How it is built

Lexifina reads the sources listed here and records each act's dated versions, and the laws that made each change, in one corpus file. `tools/build.py` writes this repository from that file, and the same corpus always gives the same commit hashes; `REPRODUCE.md` gives the details and the checks. A model (Claude) wrote Lexifina's code; it wrote no legal text, and no model runs when the history is built.

## Sources

| Source | What it gives | Used for |
| --- | --- | --- |
| [MalawiLII](https://malawilii.org) | Dated point-in-time versions (expressions) of each act, its History and amendment list, and per-provision editorial notes; its listing pages name the current version | The text and dates of every version |
| – | Archived copies of those expression pages and of MalawiLII's listing pages | Reading them |

## Licence

See [LICENSE](LICENSE). Source: MalawiLII (https://malawilii.org), licensed under the Creative Commons Attribution-NonCommercial 4.0 International licence (CC BY-NC 4.0).

MalawiLII's terms: CC BY-NC 4.0, crediting MalawiLII as the source (https://malawilii.org/terms-of-use/). Lexifina's arrangement, messages, tables and tools are CC0.

This repository is not legal advice. Malawi's laws are published in English, so there is no separate summary in another language.
