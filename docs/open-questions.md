# Open questions

Pending decisions. Resolved items move to [`decisions.md`](decisions.md) as a DEC.
Format: `OQ-nn — question (date raised)`.

- **OQ-01 — Aerial robot: Mission Planner reachability vs iNav** (2026-09-11).
  The aircraft is to be treated as an aerial robot reachable from Mission Planner,
  in the same sense as the ground robots in wk-robotics. Mission Planner is a
  MAVLink ground station. iNav's MAVLink implementation is transmit-only per the
  iNav telemetry docs: Mission Planner can display iNav telemetry but cannot upload
  missions, change parameters or command the aircraft. Full two-way control needs
  ArduPilot, which reverses DEC-01. The hardware supports either; the MicoAir743
  V2 ships with ArduPilot preloaded. Options:
  1. ArduPilot: full Mission Planner integration and EKF3 Loiter, at the cost of
     firmware commonality with the 5" quad and a harder tune.
  2. iNav with MAVLink telemetry out: Mission Planner as a read-only feed; missions
     and params stay in iNav Configurator.
  3. iNav now, ArduPilot later if the robot use case grows.

  Decide once hardware is in hand and iNav's POSHOLD has been evaluated. Until
  then the scaffold and [`setup-inav.md`](setup-inav.md) stay on iNav.
