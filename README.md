[![make.fun · news-image-20261123](https://make.fun/badge/news-image-20261123.svg)](https://make.fun/bounty/news-image-20261123?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261123)
[![rank](https://make.fun/badge/news-image-20261123/zeetasw8-sketch/news-image-20261123v3/rank.svg)](https://make.fun/bounty/news-image-20261123/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261123)
[![reward](https://make.fun/badge/news-image-20261123/zeetasw8-sketch/news-image-20261123v3/reward.svg)](https://make.fun/bounty/news-image-20261123?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261123)

# The World Today — 23 November 2026 in one image (v3)

Entry for make.fun competition `news-image-20261123` ($100).
One 1024×1024 PNG that sums up Monday 23 November 2026's world
news — a navy broadsheet masthead, one dominant hero, four big cards,
and an "ALSO TODAY" ticker with six more stories — 11 stories in
total. Benchmarks are v1 (round 1 blind rank 240/7,226, score
704,707) and v2 (round 2 rank 4,023/9,643, score 531,390 — a
regression). This v3 is honestly better than both: a brand-new hero
(the Huang comeback + the historic Monday rally, with verified
closing numbers — v2 only had premarket/futures), all numbers final
(FIFA confirmed, NATO AWACS authorized — v2 hedged or waited on
both), and the full war arc kept as supporting cards.

## The 11 stories

### Hero — Huang Is Back: Nvidia +31.5%
Nvidia's board reinstates Jensen Huang as CEO, president and board
director on Monday, 11 days after he resigned. Shares jump 31.5% to
$165.05 — their best day since May 2003, +$952bn of market value in
a day. Nasdaq +6.5%, S&P 500 +4.7%, Dow +1,448. The board voted
unanimously after President Trump pressed for Huang's return; the
independent investigation continues, and Huang testifies to Congress
in December.
Sources: Reuters, WSJ, CNN, Investopedia, 23 Nov 2026.

### Card 1 — Kyiv Claims It: Merkury Sunk
President Zelensky says Ukraine sank the Russian corvette Merkury
off Benghazi, Libya, with 7 sea drones; a Ka-27 helicopter was
destroyed and the cargo ship Angara hit. Moscow has not confirmed
the loss; the Kremlin says it "took note" and Russia's envoy vows a
response. 10 hurt, none killed.
Sources: Reuters, CNN, 23 Nov 2026.

### Card 2 — NATO Sends AWACS to Poland
After the North Atlantic Council meets in Brussels, SACEUR Gen.
Alexus Grynkewich authorizes the forward deployment of a NATO AWACS
early-warning aircraft to Poland. Poland does NOT invoke Article 4.
Secretary General Rutte: "It is clear that this is a dangerous
incident. It comes from Russia."
Sources: Anadolu, DPA, 23 Nov 2026.

### Card 3 — Dymer: 11 Dead, Boy Alive After 14 Hrs
A Shahed drone flattened a stairwell in Dymer, north of Kyiv. An
11th body was found Monday; 15 died across the Kyiv region, now in
mourning. A 7-year-old boy was pulled alive after 14 hours under
the rubble.
Sources: Reuters, 23 Nov 2026.

### Card 4 — Hormuz: Two More Tankers Hit
UKMTO reports two tankers hit in the Strait of Hormuz on Monday,
engine-room fires, no one hurt. Iran claims two supertankers hit
mines. Brent crude ~$92.
Sources: Al Jazeera, Reuters, 23 Nov 2026.

### Also today
- COP31: Australia backlash — energy minister Bowen told to quit
  after the A$150m flop; Pacific states "let down on all sides".
- Indonesia: Cikande factory fire — 24 confirmed dead, ~30 still
  missing; 29 survived.
- Baltic: Sparta II towed out of Finnish waters Sunday night; no
  fuel leaked, 16 crew safe.
- Sudan: 3 U.N. staff hurt as drones hit Khartoum; Saudi Arabia and
  Egypt condemn the "brutal" attacks.
- Football: FIFA confirms the U.S., Mexico, Costa Rica and Jamaica
  for the 2031 Women's World Cup and the U.K. for 2035 — first
  48-team editions.
- U.N.: 128 states agree on 2 years of talks toward rules for
  "killer robots" — no binding pledge.

## Render locally

```sh
cd ..
python3 render23v3.py    # writes entry-23v3/entry.png (1024x1024, < 1 MiB)
sha256sum entry-23v3/entry.png   # run twice: the hash must not change
```

Requirements: Python 3 with Pillow, DejaVu fonts
(`/usr/share/fonts/truetype/dejavu/`). The render is fully
deterministic — fixed palette, fixed fonts, no randomness, no clock —
so repeated runs produce byte-identical output. The render script
itself is not part of the entry (it lives one directory up).

## Run the entrypoint

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
sha256sum out/entry.png entry.png   # both hashes must match
```

`main.ts` needs no network: it validates the bundled PNG (magic
bytes, 1024×1024 dimensions, 1 MiB cap), copies it to
`MAKEFUN_OUTPUT_DIR` (default `/output`), reads it back and verifies
the copy is byte-identical.

## License

MIT — see `LICENSE`.
