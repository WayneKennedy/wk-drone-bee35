# Config

iNav CLI snapshots. These are the source of truth for the aircraft's configuration.

- `diff/` — `diff all` output, one file per dated revision, named
  `YYYY-MM-DD-description.txt`. Each has a matching line in
  [`../docs/tuning.md`](../docs/tuning.md).
- `dump/` — full `dump all` snapshots, for complete restoration.

## Restoring onto replacement hardware

TBC until first tested. Intended procedure:

1. Flash the same iNav version recorded in the snapshot header, MicoAir743 V2 target.
2. In Configurator CLI, paste the latest `diff/` file, then `save`.
3. Re-verify against [`../docs/setup-inav.md`](../docs/setup-inav.md): sensor
   orientation, compass calibration, receiver failsafe, motor direction. Calibration
   values do not transfer between boards.
4. Bench check with props off before flying.

If a `diff` fails to restore cleanly, fall back to the matching `dump/` file.
