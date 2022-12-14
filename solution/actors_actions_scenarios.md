# Actors, Actions and Significant Scenarios

To illustrate the needs which the architecture must satisfy, we outline the different types of actors who will use the platform and the actions each will perform. We show the steps involved in common scenarios for these actors in the diagrams that follow.


## Actors & Actions

The identified actors and their actions are as follows:

| Actor          | Actions |
| -------------- | ------- |
| Civilian       | - Registers on the platform<br />- Receives notifications when officer available for in-person or virtual connection<br />- Sends chat requests to officers<br />- Confirms connection when platform detects officer is within 10 feet<br />- Sends virtual handshake<br />- Scans officer's QR code if they meet an officer who is not logged into platform<br />- Optionally shares connections on own social media account<br />- Chooses products in storefront for which they can redeem interaction points<br />- Receives QR code when redeeming points for discounts from local retailers without e-commerce capabilities<br />- Moves points to linked account in a business's reward program<br />- Optionally receives push notifications when near participating businesses<br />- Optionally receives notifications of events on community calendar<br />| 
| Police Officer | - Registers on the platform with a valid police department e-mail address<br />- Receives chat requests from civilians<br />- Confirms connection when platform detects civilian is within 10 feet<br />- Sends virtual handshake<br />- Presents QR code for scanning if they encounter a civilian user while not logged into platform<br />- Optionally shares connections on own social media account<br />- Chooses charity to receive points earned for interactions<br />- Optionally earmarks individual to benefit from donation<br />- Adds events to community calendar<br />|
| Charity        | - Registers on the platform<br />- Chooses products in storefront for which they can redeem interaction points<br />- Confirms eligibility of individual donation recipients (e.g., verifies that a kid participates in Big Brothers, Big Sisters program)<br />|
| Business       | - Registers on the platform<br />- Creates storefront with electronic products (e.g., gift cards) and associated point values<br />- Uses Hey, Blue! API to link to its own rewards program<br />|
| Administrator  | - Views usage statistics (number of connections, points redeemed, etc.) aggregated by zip code and across platform<br />- Manages user accounts in case of technical problems or abuse<br />|

## Architecturally Significant Scenarios

The following are the most architecturally significant scenarios/flows, derived from the Actors and Actions above, which will shape the architecture of the Hey, Blue! system.

_Click on the diagrams to make them larger._

### Legend

This legend defines all the symbols that are used throughout our diagrams.

![Legend](./../assets/scenario-legend.jpg)

### Registration

![Registration Scenario](./../assets/scenario-01.jpg)

#### ADR Links
- [01 - Limiting Storefront to Electronic Goods and Online Rebates](./adr/01-electronic-goods.md)
- [02 - Using QR Codes For Local Businesses](./adr/02-business-qr-codes.md)

### Virtual Handshake

![Virtual Handshake Scenario](./../assets/scenario-02.jpg)

#### ADR Links
- [04 - Including a Temporary Chat System for Interaction Coordination](./adr/04-chats.md)

### In-person Interaction

![Interactive Scenario](./../assets/scenario-03.jpg)

#### ADR Links
- [04 - Including a Temporary Chat System for Interaction Coordination](./adr/04-chats.md)

### Redeem Points

![Redeem Points Scenario](./../assets/scenario-04.jpg)

The TBD process off the `Yes` branch of the `Rewards?` decision is intentional, as for the first iteration of the Hey, Blue! platform, it will not fully integrate with an external business's rewards program. In addition to the technical complexity, there will need to be a partnership created between the two platforms. After the initial and successful launch of Hey, Blue!, the platform will have better leverage to entice these businesses to participate.

#### ADR Links
- [02 - Using QR Codes For Local Businesses](./adr/02-business-qr-codes.md)

### Events

![Events Scenario](./../assets/scenario-05.jpg)

This scenario is for step 7 of the police officer process, outlined in the [Hey, Blue! app requirements document](https://docs.google.com/document/d/10o-4eEzFo005pqDt_ORCztzaQCQ_9FNWYrxFasou3Eo).

### Location-less Interaction

![Locationless Interaction Scenario](./../assets/scenario-06.jpg)

#### ADR Links
- [06 - Using QR Codes for In-Person Interactions Without Location Tracking](./adr/06-interaction-no-location.md)

### Administrator

![Adminitrator Scenario](./../assets/scenario-07.jpg)
