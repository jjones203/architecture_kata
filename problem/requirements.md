# Requirements

## Business Goals
As stated in the [requirements doc](https://docs.google.com/document/d/10o-4eEzFo005pqDt_ORCztzaQCQ_9FNWYrxFasou3Eo/edit#), the Hey, Blue! mobile app and website will enable:
- Civilians and law enforcement officers to have positive interactions, which will be rewarded with Hey, Blue! points
- Civilians to exchange Hey, Blue! points for goods, services, and discounts
- Law enforcement officers to donate points to charities, optionally earmarking specific recipients
- Charities to exchange donated points for goods, services, and discounts
- Hey, Blue! administrators to view platform usage statistics

## Business Requirements
We have prioritized the platform's capabilities: a minimum viable product must include those which are core to Hey, Blue!'s vision. Other features can be added in later phases.

### Short Term
- Arrange in-person interactions between officers and civilians
- Facilitate virtual interactions between officers and civilians
- Reward officers and civilians with points for interactions
- Publicize interactions on Hey, Blue! social media, with option for users to publicize on their own social media accounts
- Allow officers to donate their points to charities
- Allow civilians and charities to redeem points for electronic gift cards or rebates
- Provide virtual storefronts for participating businesses
- Enable platform administrators to view usage statistics aggregated by zip code

### Medium Term
- Allow officers to earmark their donations for individuals confirmed as eligible by charities
- Recognize interactions that occur outside the platform using QR codes assigned to officers
- Maintain community calendar to which officers can submit events they will attend
- Notify users when they are near a participating business (subject to user opt-in)

### Long Term
- Integrate with businesses' existing rewards programs
- Expand storefronts to include physical products
- Send automated reports about platform usage to local media outlets
- Use external data sources (e.g., the FBI Crime Data API) in platform analytics
- Solicit feedback from users on how any profits from the platform should be donated

## Privacy and Safety Concerns
Users can arrange to meet in person via chat. Users cannot track each others' location in real time, and both parties must consent to chat.

### User Privacy
As a non-profit, Hey, Blue! will not be subject to some privacy laws, such as the California Consumer Privacy Act. Due to additional regulations governing children's privacy (e.g., the Children’s Online Privacy Protection Act), Hey, Blue! will require users to attest that they are at least 18 years of age when registering.

Many platform functions will generate data (e.g., location data, chat logs) which might reveal sensitive information about users. Hey, Blue! will seek to discard this information as quickly as possible after a short retention period that would allow administrators to investigate problems (e.g., to review chat logs from users accused of abusive behavior).

### Security
For its traffic, Hey, Blue! will use a Certificate Authority for its TLS certificate, e.g. [Let's Encrypt](https://letsencrypt.org). Its databases will be encrypted at rest with a robust hashing algorithm. Prior to deployment, the platform will perform a security checklist akin to [SANS Securing Web Application Technologies Checklist](https://www.sans.org/cloud-security/securing-web-application-technologies/), to cover all the security needs to protect its users' data.

### Officer Safety
All civilian-officer interactions will be posted to Hey, Blue!'s social media. However, the post will include only the users' first names or nicknames, it will not include a photo unless both parties agree, and an automatic 15-minute delay will ensure officers' locations are not trackable via social media. When an officer is logged into the mobile app with location tracking enabled, the app will send an alert after 15 minutes of inactivity; if the officer does not click on a button confirming they are active, they will be automatically logged out.
