# wk-drones

Build, configuration and maintenance records for a small fleet of DIY multirotors, and
the kit they share. One folder per aircraft; fleet-wide facts live once, in `fleet/`.

Config files are the source of truth for each aircraft: version-controlled, diffable,
restorable onto replacement hardware.

## The fleet

| Aircraft | Folder | What it is | Firmware | Family robot? | State |
|---|---|---|---|---|---|
| **Bee35** | [`aircraft/bee35/`](aircraft/bee35/README.md) | 3.5" ducted cinewhoop, SpeedyBee Bee35 Pro frame, built for a DJI-like hands-off FPV experience | iNav | No — [DEC-07](aircraft/bee35/docs/decisions.md) | Parts ordered 2026-09-11; nothing built, flashed or flown |
| **Holybro 10"** | [`aircraft/holybro-10/`](aircraft/holybro-10/README.md) | 10" build bought to carry a Raspberry Pi or Jetson wired to its flight controller | Unknown | **Yes — the fleet's only candidate** | Unknown; not yet recorded ([F-OQ-01](fleet/open-questions.md)) |
| **5" freestyle** | [`aircraft/fpv-5/`](aircraft/fpv-5/README.md) | Existing 5" freestyle quad; covers the acro use case | iNav | No | Exists and flies; build state not yet recorded ([F-OQ-01](fleet/open-questions.md)) |

**Family robot?** means: does it meet the wk-robotics criterion for an aerial robot, an
intent-tier computer commanding the flight controller. The criterion and its two
topologies (onboard, or off-board over radio) are defined once, in
[wk-robotics `docs/common.md`](https://github.com/WayneKennedy/wk-robotics/blob/main/docs/common.md#aircraft-and-the-tiers),
and the fleet-level decision applying it is [F-DEC-01](fleet/decisions.md). The
wk-robotics index lists the Holybro as a project and this repo as a supporting record;
the other two aircraft are FPV builds and appear nowhere in that index.

## Where things live

- [`AGENTS.md`](AGENTS.md) — onboarding for any assistant or contributor
- [`fleet/`](fleet/README.md) — kit shared by more than one aircraft: radio link, video,
  battery packs, tooling · [`fleet/decisions.md`](fleet/decisions.md) (`F-DEC-nn`) ·
  [`fleet/open-questions.md`](fleet/open-questions.md) (`F-OQ-nn`)
- `aircraft/<name>/` — one aircraft: `README.md`, `docs/`, `config/`, `print/`, `logs/`,
  `maintenance.md`. Decisions and open questions are per aircraft (`DEC-nn`, `OQ-nn`,
  scoped to the folder).

## Licence

[MIT](LICENSE), covering everything here that is mine. Not run as an open-source project,
but nothing restricts reuse. Third-party STLs under `aircraft/*/print/stl/` keep their
upstream licences, listed in each aircraft's `print/sources.md`.
