# Limiting Application Functionality on the Web

## Status
Accepted

## Context
The web browser API for location is more limited compared to preciseness of location from a native application for a mobile device.

## Decision
We propose to remove the ability to have in-person connection between a civilian and a police office, if any or both of the users are not using their mobile devices while tracking their location. The data available to the web browser API is too inaccurate to validate the near proximity between two individuals, especially if a user is not allowing location tracking from their browser.

## Consequences

### Pros
- Accurate geolocation informatino from a phone's GPS

### Cons
- Users cannot use the web browser to initiate in-person interactions