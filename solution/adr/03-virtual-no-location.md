# Limiting Interactions to Virtual Handshakes When No Geolocation Tracking

## Status
Accepted

## Context
Some users may access the Hey, Blue! platform from their web browser, either on their phone or from a computer. This should not prevent users from virtually connecting, when within the same zip code. However, the precision of a web browser's location API is limited compared to the location data from a native application for a mobile device.

## Decision Drivers
- How can a civilian interact with a police officer without geolocation tracking functionality on their device?
- Can a civilian interact with a police officer virtually?

## Decision
We propose to remove the ability to have in-person connection between a civilian and a police office, if either is not using the mobile app with location tracking. The data available to the web browser API is too inaccurate to validate the near proximity between two individuals, especially if a user is not allowing location tracking from their browser. The Hey, Blue! platform will allow for virtual interaction between two users who are online and have the same home zip code.

## Consequences

### Pros
- Remove another friction point for interactions
- Lower barrier of entry for users

### Cons
- Users cannot use the web browser to initiate in-person interactions
