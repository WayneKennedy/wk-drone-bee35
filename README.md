# wk-drone-bee35

Build, configuration and maintenance record for a 3.5" ducted cinewhoop on the
SpeedyBee Bee35 Pro frame, running iNav, built for stability and endurance rather
than speed.

This is a living engineering record, not a one-off build log. Config files are the
source of truth: version-controlled, diffable, and restorable onto replacement
hardware.

## Status

**Parts ordered, not yet in hand.** Nothing has been built, flashed or flown.
Every value marked TBC is unconfirmed until hardware arrives.

Intended role: an aerial robot in the [wk-robotics](https://github.com/WayneKennedy/wk-robotics)
family, eventually reachable from its mission-planning tier. That step comes after
the basic goal is met on iNav; see [DEC-06](docs/decisions.md).

## Design intent

Reference behaviour is a DJI Neo: level hover, solid position hold, predictable
stick response, returns to hold when sticks are released. The existing 5" freestyle
quad already covers the acro use case and is explicitly *not* the target here.

Priorities, in order:

1. Position and altitude hold quality
2. Flight duration
3. Video quality
4. Speed and agility (lowest, deliberately traded away)

Non-goals: racing, freestyle, sub-250g compliance, companion computer, secondary
action camera.

## Expected performance

Hypotheses, to be validated against measured figures. Where reality differs, record
it here and note why.

| Metric | Estimate | Actual |
|---|---|---|
| Dry weight | ~300 g | TBC |
| AUW with P45B pack | ~620 g | TBC |
| Hover throttle | ~1/3 | TBC |
| Flight time | 12–18 min | TBC |

Flight time is materially less than an uncaged build would give. The cage is the
cost of a machine that is safe to fly near people and survives contact.

## Where things live

- [`AGENTS.md`](AGENTS.md) — onboarding for any assistant or contributor

- [`docs/bom.md`](docs/bom.md) — bill of materials, suppliers, order dates
- [`docs/wiring.md`](docs/wiring.md) — port map, solder notes, jumper settings
- [`docs/setup-inav.md`](docs/setup-inav.md) — first flash through maiden checklist
- [`docs/decisions.md`](docs/decisions.md) — architecture decision records
- [`docs/open-questions.md`](docs/open-questions.md) — pending decisions
- [`docs/tuning.md`](docs/tuning.md) — PID and filter changes, with rationale
- [`config/`](config/README.md) — iNav `diff all` and `dump all` snapshots, and how to restore
- [`print/sources.md`](print/sources.md) — upstream URLs and licences for every STL
- [`maintenance.md`](maintenance.md) — crashes, repairs, parts replaced

## Conventions

- Every `config/diff/` file is named `YYYY-MM-DD-description.txt`, with a one-line
  note in `docs/tuning.md` saying what changed and why.
- Never commit an untested config without marking it as such.
- Link decisions in `docs/decisions.md` from wherever they are referenced.
- Blackbox logs, firmware binaries and large STL archives are gitignored.

## Licence

[MIT](LICENSE), covering everything here that is mine. Not run as an open-source
project, but nothing restricts reuse if it is useful to you. Third-party STLs in
`print/stl/` keep their upstream licences, listed in [`print/sources.md`](print/sources.md).
