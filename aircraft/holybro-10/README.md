# Holybro 10"

A 10" multirotor on Holybro hardware, **bought specifically to carry a Raspberry Pi or
Jetson hard-wired to its flight controller.** That makes it the fleet's only candidate
for a wk-robotics aerial robot ([F-DEC-01](../../fleet/decisions.md)), and the only
aircraft the [wk-robotics index](https://github.com/WayneKennedy/wk-robotics/blob/main/docs/projects.md)
lists as a project.

## Status

**Unknown — not yet recorded.** Frame, flight controller, firmware, receiver, video,
companion computer, wiring and build state are all to be written down by the owner
against the hardware ([F-OQ-01](../../fleet/open-questions.md)). Nothing on this page
beyond the first paragraph is established.

## Role in the family

Onboard-intent topology: the companion computer is the intent tier, the flight controller
the reflex tier, wired together. See wk-robotics
[`docs/common.md`](https://github.com/WayneKennedy/wk-robotics/blob/main/docs/common.md#aircraft-and-the-tiers)
for what that permits, and the same document's compute pattern for the tiers themselves.
How it joins the family's topic contract is unrecorded.

## Where things live

Follows the shape of [`../bee35/`](../bee35/README.md). Files are created when there is
content for them, not before.
