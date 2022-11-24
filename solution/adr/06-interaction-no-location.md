# Using QR Codes for In-Person Interactions Without Location Tracking

## Status
Accepted

## Context
The requirements state a civilian and a police officer must have the ability to connect without the police officer needing to be found, i.e. actively tracked by the Hey, Blue! platform. The civilian will be able to scan the officer's assigned QR code to validate the interaction and for the points to be awarded.

## Decision Drivers
- How does the platform allow for ad-hoc interactions without the police officer being tracked?
- How does the platform make these ad-hoc interactions seamless?

## Decision
There will be instances when a police office does not want the Hey, Blue! platform to be actively tracking their location, but they may have ad hoc in-person interaction. Instead of having the police officer turn on their location to validate the proximity betweem them and the civilian, the civilian can just scan the officer's QR code and the backend will validate the interaction using that information instead.

## Considered Options
[Near-field communication](https://en.wikipedia.org/wiki/Near-field_communication) is a set of communication protocols that enables communication between two electronic devices over a distance of 4 cm or less. Even though it is prevalent, it is not a guaranteed feature especially in mid- to low-range smartphones. Relying on a camera lens for ad-hoc interactions is a safer alternative to allow these kind of interactions to the majority of the user base, if not all of it.

## Consequences

### Pros
- Better safety mechanism for the police officers
- Seamless interaction possibility between an officer and a civilian
