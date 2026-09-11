# Open questions

Pending decisions. Resolved items move to [`decisions.md`](decisions.md) as a DEC.
Format: `OQ-nn — question (date raised)`.

- **OQ-01 — Aerial robot: how the fleet mission planner reaches it, and what that
  means for firmware** (2026-09-11). The aircraft is to be treated as an aerial robot
  in the wk-robotics family, reachable from the mission planner. In that family
  "Mission Planning" is the aspirational off-robot third tier above reflex and intent
  (wk-robotics `docs/common.md`, `docs/ideas.md`), speaking ROS 2 over the
  [topic contract](https://github.com/WayneKennedy/wk-robotics/blob/main/docs/common.md#the-topic-contract).
  It may also mean ArduPilot's Mission Planner ground station. Either reading
  favours ArduPilot and conflicts with DEC-01:
  - **ArduPilot** has a native ROS 2 interface (AP_DDS, micro-ROS XRCE-DDS over
    serial or UDP, ArduPilot 4.5+) and full two-way MAVLink, so Mission Planner and
    a ROS 2 mission tier can both command it. The MicoAir743 V2 ships with it.
  - **iNav** has no ROS 2 interface. Its MAVLink implementation is transmit-only per
    the iNav telemetry docs: a ground station can display telemetry but cannot
    upload missions, change parameters or command the aircraft.
  - A third path, iNav now and ArduPilot when the fleet role is real, keeps DEC-01's
    commonality with the 5" quad for the maiden and tune.

  Also unlike every other robot in the family, the flight controller is reflex and
  intent tier in one MCU; there is no on-board Pi. How it joins the topic contract
  is part of this question.

  Decide once hardware is in hand. Until then the scaffold and
  [`setup-inav.md`](setup-inav.md) stay on iNav.
