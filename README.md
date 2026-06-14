# The Drop — DJs vs. the U.S. Economy

**Does the rise and fall of DJ culture move with the economy, or to its own beat?**

An interactive explorer that lines up the electronic-music scene against U.S. economic
indicators from 2007–2025. Toggle data "channels" on a mixer-style console, index
everything to a common base year so different units share one axis, see recessions
shaded in, and switch to a correlation view to test the relationship directly.

It's a single self-contained `index.html` — open it in a browser or drop it on GitHub
Pages, no build step or server needed.

---

## What it shows

- **Timeline view** — each series indexed to 100 at a base year you choose, so the
  electronic-music industry (in $B), unemployment (in %), and real GDP (in $T) can be
  read on one scale. Recessions (2008–09 and 2020) are shaded.
- **Correlation view** — a scatter of a DJ metric against an economic one, with a fitted
  line and the Pearson correlation, plus a plain-language reading of what it means.
- **Context cards** — the BLS DJ-employment numbers, including why the official count
  misses most of the profession.

## What the data says

Indexed to 2019, the electronic-music industry fell to **47** in 2020 (a ~53% COVID
crash), clawed back to 82 in 2021, then climbed to **207** by 2025. Against the economy
over the shared years, electronic-music revenue correlates at about **r = +0.80 with real
GDP** and **r = −0.75 with unemployment** — the scene grows when the economy is strong and
contracts when joblessness spikes. With only ~7 overlapping years, treat that as a strong
hint rather than proof.

## Data & sources

| Series | What it is | Source |
|---|---|---|
| Electronic music revenue | Global industry value, $B, annual | IMS Electronic Music Business Report (MIDiA Research) |
| DJ employment (formal) | Wage & salary "Disc Jockeys, Except Radio" (SOC 27-2091) | BLS Occupational Employment & Wage Statistics |
| DJ employment (total) | Includes self-employed (~47%) | BLS Occupational Outlook Handbook |
| Unemployment rate | Annual average, % | BLS / FRED `UNRATE` |
| Real GDP | Chained 2017 $, annual | FRED `GDPC1` |
| Recession dates | Shaded bands | NBER |

All values are in `data.csv`. The BLS DJ pages are per-year at
`bls.gov/oes/<year>/may/oes272091.htm`; FRED series download as CSV from `fred.stlouisfed.org`.

## Honest caveats

- **DJs are mostly self-employed**, so the formal BLS wage count (~5–6k) badly undercounts
  the real workforce (~15k in 2024). The viz shows both.
- **Industry revenue is an annual estimate** and is sometimes restated between report
  editions; a few years are left as gaps rather than guessed.
- **Real GDP values are approximate** — refresh from FRED for exact current-vintage figures.
- **Correlation ≠ causation**, and ~7 shared years is a small sample. The correlation view
  is a conversation starter, not an econometric claim.

## Extending it

The most natural addition is a **DJ search-interest line from Google Trends** (a long, free
proxy for the hobby side, 2004–present). Export "DJ" interest-over-time as CSV from
`trends.google.com`, then add it as a new entry in the `SERIES` object near the top of the
`index.html` script — give it `group:"culture"` and it'll appear as a new channel
automatically.

## Run / host

Just open `index.html` in any browser. To publish: push to a repo, enable GitHub Pages,
and it's live. The fonts load from Google Fonts when online and fall back to system fonts
offline.
