# A time series exploring the state of DJ-ing and the broader U.S. economy

There's been a noticeable rise in the number of self-proclaimed disc jockeys (DJs),
seemingly from the rapid growth of gig workers and the slowing rate of expansion of
the traditional economy. I'm interested in what the numbers are indicating.

[This](https://keziasetokusumo.github.io/dj_economic_indicator/) is an interactive explorer that lines up the electronic-music scene against some
U.S. economic indicators from ~2007–2025. Toggle data "channels" on a mixer-style console, index
everything to a common base year so different units share one axis, see recessions
shaded in, and switch to a correlation view to test the relationship directly.

---

## What it shows

- **Timeline view** — each series indexed to 100 at a base year you choose, so the
  electronic-music industry (in $B), unemployment (in %), and real GDP (in $T) can be
  read on one scale. Recessions (2008–09 and 2020) are shaded.
- **Correlation view** — a scatter of a DJ metric against an economic one, with a fitted
  line and the Pearson correlation, plus a plain-language reading of what it means.
- **Barriers to entry** — the cost of a starter DJ setup over time, on a log scale, from
  the vinyl era to phone-and-streaming. Shows how digital technology collapsed the cost of
  getting behind the decks.
- **Two tiers** — the pay gap between the world's #1 DJ (Forbes Electronic Cash Kings) and a
  typical working DJ (BLS median), on a log scale. Hover any year for the multiple between
  them.
- **The local gig** — the unit economics of a single show: gross fee vs. actual take-home
  across a cafe set, a bar/club night, and a self-promoted event. Shows how venue, PA, and
  promo costs squeeze per-show profit — and can turn a packed self-promoted night into a loss.
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
| DJ setup cost | Representative entry-level rig, illustrative | Retail prices (vinyl, CDJ, controllers, apps) |
| Top DJ earnings | Highest-paid DJ, $M, 2012–2019 | Forbes Electronic Cash Kings |
| Working DJ pay | Median DJ wage, annualized | BLS OEWS 27-2091 |
| Per-gig economics | Gross fee vs. take-home, illustrative | Booking-rate guides (Bark, The Bash, Thumbtack) + venue/PA rental prices |


## Data limitations

- **DJs are mostly self-employed**, so the formal BLS wage count (~5–6k) badly undercounts
  the real workforce (~15k in 2024). The visualization shows both.
- **Industry revenue is an annual estimate** and is sometimes restated between report
  editions; a few years are left as gaps rather than guessed.
- **Real GDP values are approximate** — refresh from FRED for exact current-vintage figures.
- **Setup costs are illustrative** — representative retail prices at each era, not a
  continuous price index, and they assume you already own a laptop/phone for the digital eras.
- **The pay gap mixes sources** — top-tier earnings (Forbes) and the working-tier median
  (BLS) are measured differently, and the Forbes list stopped after 2019. The working-DJ
  median is a small, noisy survey shown roughly flat.
- **Per-gig economics are illustrative** — representative gross fees and venue/PA/promo costs
  from booking guides, not measured accounts. Real numbers swing widely by city, night, and
  draw; the self-promoted loss is a common-but-not-universal outcome.
- **Correlation ≠ causation**, and ~7 shared years is a small sample. The correlation view
  is a conversation starter, not an econometric claim.
