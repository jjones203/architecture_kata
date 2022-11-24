# Limiting Storefront to Electronic Goods and Online Rebates

## Status
Accepted

## Context
One of the requirements for the platform is to allow businesses to create a storefront on the application to encourage users to redeem their points. If operating these storefronts requires technical expertise and inventory management, business will have less incentive to participate. Likewise, a simpler solution will be more feasible and economical for Hey, Blue! to implement, particularly in the platform's intial iteration.

## Decision Drivers
- What is the simplest way that the Hey, Blue! platform can allow users to redeem interaction points for rewards from businesses?
- Can we meet this requirement without the implementation of additional functionality (e.g., inventory management, shipping and tracking) on the part of either Hey, Blue! or participating businesses?

## Decision
Providing storefronts on the Hey, Blue! platform puts the onus on the external businesses to provide a (or an additional) technical solution for their inventory and distribution of goods. Providing these entities with a simple application programming interface (API) and templates for listing gift cards and promo rebate codes removes the need to manage SKUs (stock-keeping units) for the businesses and Hey, Blue!'s technical team.

## Considered Options
The Hey, Blue! requirements imply users can order physical goods through the platform: "Businesses should have a catalog of items that they are offering and the point value assigned to each item available.... User applies points for product, i.e.: new shoes." In order to provide this service through Hey, Blue! directly, the platform would need to handle inventory, payment, shipping options, etc. We decided this seemed like an excessive investment relative to the feature's importance. Allowing users to redeem points for electronic rebates and gift cards still incentivizes interactions through rewards from participating businesses but with fewer logistical hurdles. 

In future iterations, integration with an e-commerce service provider such as Shopify could allow users to purchase goods and services within the Hey, Blue! platform. However, this may discourage some businesses from participating in Hey, Blue! because they would likely need to subscribe to the e-commerce service.

## Consequences

### Pros
- Seamless adoption from external businesses
- Reduce technical complexity for first implementation of the platform

### Cons
- Less choice for the user
- Less engagement for the user to redeem their points


