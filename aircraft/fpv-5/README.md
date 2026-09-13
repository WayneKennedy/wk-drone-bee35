# 5" freestyle

The existing 5" freestyle quad. It covers the acro use case, which is why the Bee35
deliberately does not ([Bee35 README](../bee35/README.md)), and it runs iNav, which is
why the Bee35 does too ([Bee35 DEC-01](../bee35/docs/decisions.md)).

Not a wk-robotics robot: a human on the sticks ([F-DEC-01](../../fleet/decisions.md)).

## Status

**Exists and flies; build state not recorded.** Frame, flight controller, iNav version,
receiver, video and maintenance history are to be written down by the owner against the
hardware ([F-OQ-01](../../fleet/open-questions.md)).

## Idea, not a plan

The owner has floated fitting a small Raspberry Pi (a Zero 2 W or similar; which one is
unconfirmed) to this airframe. If it were wired to the flight controller as an intent
tier, the aircraft would cross the family's robot criterion. No decision has been taken,
nothing has been bought, and no payload or power budget has been done.

## Where things live

Follows the shape of [`../bee35/`](../bee35/README.md). Files are created when there is
content for them, not before.
