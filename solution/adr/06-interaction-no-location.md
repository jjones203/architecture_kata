# Using QR Codes for In-Person Interactions Without Location Tracking

## Status
Accepted

## Context
The requirements state a civilian and a police officer must have the ability to connect without the police officer needing to be found, i.e. actively tracked by the Hey, Blue! platform. The civilian will be able to scan the officer's assigned QR code to validate the interaction and for the points to be awarded.

## Decision Drivers
- How does the platform allow for ad-hoc interactions without the police officer being tracked?
- How does the platform make these ad-hoc interactions seemless?

## Decision
There will be instances when a police office does not want the Hey, Blue! platform to be actively tracking their location, but they may have ad hoc in-person interaction. Instead of having the police officer turn on their location to validate the proximity betweem them and the civilian, the civilian can just scan the officer's QR code and the backend will validate the interaction using that information instead.

## Consequences

### Pros
- Better safety mechanism for the police officers
- Seamless interaction possibility between an officer and a civilian
