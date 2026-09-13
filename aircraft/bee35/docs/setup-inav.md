# iNav setup

First flash through maiden. Checklist steps are stubs until hardware is in hand;
the settings of note below are the target configuration and are fixed by the
[decisions](decisions.md).

## Firmware

- iNav 8.0 or later. The MicoAir743 V2 target was added at 8.0.
- The board ships with ArduPilot preloaded. Reflash to iNav (DEC-01).

## Settings of note

- **Disable the FC's internal compass.** Use only the external compass on the GPS
  mast. ESC current on a 30.5 mm stack makes the onboard mag a liability for POSHOLD.
- **MTF-01P orientation differs between iNav and ArduPilot.** Follow the
  iNav-specific direction and verify in Configurator that flow values move the
  right way before the maiden.
- **Battery: Li-Ion, 4S.** Set cell thresholds for Molicel P45B chemistry, not LiPo
  defaults. Full 4.2 V/cell, land at 3.3 V/cell (13.2 V pack), critical 3.0 V/cell.
- **Modes.** One 3-position switch: Angle → Angle + ALTHOLD → POSHOLD. NAV RTH on its
  own switch. Failsafe → RTH once GPS is proven.

## Checklist

Stub. Fill in as each step is done, in order.

1. Flash iNav 8.x, MicoAir743 V2 target
2. Ports: assign UARTs per [`wiring.md`](wiring.md)
3. Receiver: CRSF, verify channel map and failsafe behaviour
4. GPS and external compass; disable internal compass; calibrate compass away from
   the bench
5. MTF-01P: MSP, verify orientation and live flow/range values
6. Walksnail: MSP DisplayPort, OSD layout
7. Battery: Li-Ion profile and P45B thresholds
8. Motors: direction and order, props off
9. Modes and failsafe
10. Bench hover checks, then maiden in Angle only, then ALTHOLD, then POSHOLD

## Optional: pitch-stabilised camera

Standard cinewhoop uptilt (~20°) exists to correct for nose-down forward flight and
is wrong for a machine that hovers level. Try low-tilt printed inserts (0/5/10°)
first. POSHOLD keeping the airframe level may remove the need entirely.

If a tilt axis is still wanted: iNav removed the named `SERVO_TILT` feature at 2.0.
It is now configured in the Mixer tab with a servo rule sourced from *Gimbal Pitch*,
plus CAMSTAB mode for accelerometer-based stabilisation, and an AUX channel mapped
to the same servo for manual look-down. Verify the MicoAir743 exposes usable servo
outputs in multirotor configuration first; some boards do not.

Do not buy SpeedyBee's 28 g "shock-absorbing gimbal" accessory expecting this. It
is passive damping only.
