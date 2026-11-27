# Structure

How this repository is laid out. Folder and file names are in English, the language of Malawi's legislation.

| Folder | What it holds | Example |
| --- | --- | --- |
| `constitution/` | The Constitution of the Republic of Malawi (Act 20 of 1994), one file per section | `constitution/sec-016.md`: section 16, the right to life |
| `acts/<year>/<number>-<short title>/` | Acts of Parliament, by the year and number of the Act as enacted | `acts/2000/006-employment-act/sec-044.md`: section 44 of the Employment Act (Act 6 of 2000) |
| `subsidiary/<year>/<number>-<short title>/` | Subsidiary legislation (Government Notices, rules, regulations, orders), by year | `subsidiary/2003/fertilizers-regulations-2003/` |
| `data/`, `tools/` | Tables (`laws.csv`, `commits.csv`) and the tools (`tools/on.py`) | |

No folder holds more than 1,000 entries.

Inside each act:

- one file per section (`sec-044.md`), schedule (`schedule-01.md`, `sch-01.md`) or, where the sections could not be split from the source, one `text.md`;
- `long-title.md` or `preamble.md`: the long title and enacting words;
- `README.md`: the act's provisions and where its text comes from.

Each commit is one version of one act or instrument, dated noon Africa/Blantyre on the day it took effect, with the day in its `In-force:` trailer and the reason for that day in `In-force-basis:`. Versions before 1970 are stamped 1 January 1970 (git cannot store earlier dates); their subject and `In-force:` trailer carry the real day. Copies from a secondary source carry `Source-status: secondary copy (...)`; text layers the publisher made by OCR carry `Text-source: publisher OCR`.

Acts that MalawiLII dated (the Constitution and 35 others) moved from top-level folders (`employment/`) to `acts/<year>/<number>-<short title>/` in one commit on 27 November 2026 that only renames files.
