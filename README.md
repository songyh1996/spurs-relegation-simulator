# Spurs · The Final Five

An interactive simulator for Tottenham Hotspur's 2025/26 relegation run-in.

[**Open the live demo →**](https://songyh1996.github.io/spurs-relegation-simulator/)

![Spurs Final Five](https://img.shields.io/badge/Premier%20League-2025%2F26-132257) ![Status](https://img.shields.io/badge/status-live-2ed573) ![No build](https://img.shields.io/badge/build-zero%20deps-c4a661)

## What it does

As of matchweek 33 (April 19, 2026), Spurs sit 18th on 31 points — inside the relegation zone for the first time since January 2009. They have **five matches left** to escape.

This page lets you:

- **Call each of Spurs' five remaining fixtures** (W / D / L). The board recalculates instantly.
- **Watch the relegation maths update live** — probability of finishing 20th, 19th, 18th, 17th, or ≤16th.
- **Run 10,000 Monte Carlo simulations** of the rest of the season under whatever scenario you've locked.

## Spurs' run-in

| # | Date | Opponent | Venue |
|---|---|---|---|
| 1 | Sat 25 Apr | Wolves | Away |
| 2 | Sun 3 May | Aston Villa | Away |
| 3 | Mon 11 May | Leeds | Home |
| 4 | Sun 17 May | Chelsea | Away |
| 5 | Sun 24 May | Everton | Home |

## How the model works

For each Spurs fixture, win/draw/loss probabilities are computed from each team's season points-per-game with a home advantage of ±12% on the win share. Locking an outcome forces that result in every simulated season.

Other clubs in the relegation race draw their remaining results from a multinomial calibrated to season PPG (draws peak around PPG ≈ 1).

Final positions are sorted by total points; ties are broken randomly as a proxy for goal difference.

## Tech

Single self-contained HTML file. No build step, no dependencies, no framework. Just open `index.html` in a browser.

## Run locally

```bash
git clone https://github.com/songyh1996/spurs-relegation-simulator.git
cd spurs-relegation-simulator
open index.html
```

## Data sources

- [Sky Sports — Premier League Table](https://www.skysports.com/premier-league-table)
- [ESPN UK — Tottenham Fixtures](https://www.espn.co.uk/football/team/fixtures/_/id/367/tottenham-hotspur)

Snapshot taken April 19, 2026 (matchweek 33).

## License

MIT
