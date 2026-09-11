# Decisions

Architecture decision records. Each captures the decision, the alternatives and the
reasoning, not just the outcome. Format: `DEC-nn — decision (date)`.

- **DEC-01 — iNav over ArduPilot** (2026-09-11). ArduPilot's EKF3 Loiter is the
  stronger position hold and was the original plan. Chose iNav for firmware
  commonality with the existing 5" quad, a familiar configurator, and an easier
  tune. Hardware is identical either way, so ArduPilot remains a reflash away if
  iNav's hold disappoints.

- **DEC-02 — Bee35 Pro over standard Bee35** (2026-09-11). Not a preference: the
  standard version was out of stock. Turned out favourable. The alloy heatsink has
  20×20 mounting holes and takes the Walksnail VTX, which runs hot in a ducted frame
  with poor airflow.

- **DEC-03 — 4S over 6S** (2026-09-11). Motors were mis-ordered as 1700KV (the 6S
  variant) and exchanged for 3000KV. Considered building 6S P45B packs instead:
  ~50% more energy for ~50% more pack mass nets only ~10% endurance gain, at ~£60
  and a second pack format. Fleet commonality on the existing 4S1P P45B packs won.

- **DEC-04 — MTF-01P over MTF-02P** (2026-09-11). The -02P was the original spec and
  has been out of stock for months. The -01P is the better sensor anyway: 12 m lidar
  vs 6 m, 100 Hz vs 50 Hz. Its only disadvantage is ~3 g, irrelevant at this AUW.

- **DEC-05 — Flywoo GM10 Mini over Matek M10Q-5883** (2026-09-11). Matek stock
  unavailable in the UK due to export restrictions. Same M10050 + QMC5883L silicon,
  smaller patch antenna.
