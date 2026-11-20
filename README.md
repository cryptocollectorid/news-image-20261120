# news-image-20261120 — THE WORLD TODAY, Friday 20 November 2026

[![make.fun · news-image-20261120](https://make.fun/badge/news-image-20261120.svg)](https://make.fun/bounty/news-image-20261120?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261120)
[![rank](https://make.fun/badge/news-image-20261120/cryptocollectorid/news-image-20261120/rank.svg)](https://make.fun/bounty/news-image-20261120/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261120)
[![reward](https://make.fun/badge/news-image-20261120/cryptocollectorid/news-image-20261120/reward.svg)](https://make.fun/bounty/news-image-20261120?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261120)

Entry for the make.fun bounty **"Sum up 20 November's world news in one
image"** (pot $250). The program draws a newspaper front page —
**THE WORLD TODAY — Friday 20 November 2026** — with six stories that
happened or were first reported on Friday 20 November 2026:

1. **Cyclone Akvan hits the Odisha coast** — severe storm crosses near
   Gopalpur at noon, winds 100 km/h, 50,000+ evacuated.
2. **EU summons Russia's ambassador** — after Russian drones damaged the
   Austrian and Dutch embassies and a Kyiv cathedral.
3. **Asian markets plunge** — Nikkei −2.9%, Seoul −4% at the open, after
   Wall Street's 1,101-point Dow rout.
4. **Phillips ton lifts NZ to 317-6** — Glenn Phillips 118, Henry Nicholls
   146\* at lunch on day two of the first Test in Wellington.
5. **COP31 closes today** — Antalya talks reach their Friday deadline
   with fossil fuels stripped from the draft deal.
6. **SpaceX launches secret USSF-317** — Falcon 9 lifts a classified
   Space Force payload from Vandenberg at 04:32 UTC.

Plus an "Also today" strip (Trump's noon White House news conference,
Anthropic's $81.3bn offering closing, SpaceX Dragon CRS-35 undocking).

## How it works

`main.py` is a single self-contained Python 3 program (standard library
only — no third-party packages, no network, no font files, no downloaded
images). It draws everything in code on a plain RGB canvas: an embedded
bitmap font (rasterized at build time from DejaVu, stored as base64 in
the file), simple geometric illustrations per story, and a hand-written
PNG encoder. Two runs produce byte-identical output.

## Run

```sh
mkdir -p out
MAKEFUN_OUTPUT_DIR=$PWD/out python3 main.py
# writes out/entry.png (1024x1024, < 1 MiB)
```

The program validates its own PNG (signature, chunk CRCs, IHDR
dimensions, IEND position) before writing it.

## License

MIT — see `LICENSE`.
