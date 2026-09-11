# wk-drone-bee35 — agent / contributor onboarding

Read this first. It is provider-neutral: every AI assistant or human working here
reads this same file.

## Family rules

This repo is one project in the wk-robotics family. The family rules, the 4Cs
standard, and the placement rule (a fact lives in exactly one place) are in
[wk-robotics `AGENTS.md`](https://github.com/WayneKennedy/wk-robotics/blob/main/AGENTS.md)
and apply here in full. In short: correct, complete, coherent, concise. The repo is
the memory; nothing durable lives only in chat or in one assistant's private memory.

## What this repository is

The build, configuration and maintenance record for a 3.5" ducted cinewhoop on a
SpeedyBee Bee35 Pro frame. See [`README.md`](README.md) for intent and status.

## Where things live

- [`README.md`](README.md) — intent, priorities, status, expected vs actual performance
- [`docs/bom.md`](docs/bom.md) — bill of materials
- [`docs/wiring.md`](docs/wiring.md) — port map and solder notes
- [`docs/setup-inav.md`](docs/setup-inav.md) — flash to maiden
- [`docs/decisions.md`](docs/decisions.md) — **decided**, as DEC-nn
- [`docs/open-questions.md`](docs/open-questions.md) — **open**, as OQ-nn
- [`docs/tuning.md`](docs/tuning.md) — every PID/filter change, one line per config diff
- [`config/`](config/README.md) — CLI `diff all` and `dump all` snapshots; the source of truth for the aircraft
- [`print/sources.md`](print/sources.md) — STL provenance
- [`maintenance.md`](maintenance.md) — crashes, repairs, replacements

## Conventions

- **Never state an open question as settled.** DEC and OQ are separate files.
- **TBC means TBC.** Do not fill in a value that has not been confirmed against
  hardware, an invoice or a datasheet.
- **Config discipline.** Every `config/diff/` file is `YYYY-MM-DD-description.txt`
  with a matching line in `docs/tuning.md`. An untested config is marked untested.
- **Measured beats plausible.** Performance figures carry the date and conditions.
- **This repo is private.** It may hold prices and supplier detail; it must not hold
  credentials.
