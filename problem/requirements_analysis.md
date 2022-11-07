# Requirement Analysis
Here we map technical requirements to non-functional requirements, which are ordered by importance. This analysis takes the following format:

*Business requirement*

- Technical capability required of platform

  **Non-functional requirement of platform**

---

*The platform must facilitate interactions between civilians and officers: in-person interactions when users are near one another or virtual interactions when officers are unavailable for in-person connection. Civilians can find officers that are willing to connect, but officers cannot find civilians.*
- The platform must track users' availability and locations. 
- The platform must enable synchronous communication so users can arrange to meet in-person or connect virtually.

  **(1) Availability** - The platform must allow users to connect with each other at any time of day or night. Frequent outages could discourage use of the platform and prevent Hey, Blue! from building a user base. We will aim for 99% uptime.

  **(2) Responsiveness** - The platform must handle requests quickly enough to facilitate chats between users. We will aim for most typical user requests to take 0.1-0.2 milliseconds from the user initiating the request to the app responding to the request, with an outside limit of 1 second for more complex transactions. 

  **(3) Workflow** - For safety and privacy reasons, the platform will only connect users after both parties accept the connection request, which must be initiated by the civilian. The platform must ensure requests and responses occur in the correct order.
<br>
<br>

*Police departments in several major U.S. cities have expressed interest in Hey, Blue! All officers within participating departments and all adults who live in the communities they serve are eligible to register for Hey, Blue!*
- When a user registers as an officer, the platform must confirm that their email address is associated with a participating department.
- The platform architecture should be robust enough to handle rapid growth as Hey, Blue! expands to new cities.

  **(4) Scalability** - The platform must maintain availability and responsiveness as its user base grows.

  **(5) Concurrency** - As the Hey, Blue! community grows, more users will try to connect with each others through the platform at any given time. The platform must be able to handle these simultaneous requests.
<br>
<br>

*The platform rewards interactions with points: civilians and officers earn points for interacting. Officers can donate their points to a charity, and civilians and charities can exchange points for discounts, goods, or services offered by businesses.*

- The platform must track how many points each user has accrued.

- The platform must provide storefronts where businesses can offer discounts, goods, or services to users in exchange for various numbers of points.

- The platform must deduct the appropriate number of points from a user's account when the points are redeemed through a storefront.

  **(6) Data Integrity** - The platform must maintain correct records of users' correct point balances and the points associated with each item in a storefront.
<br>
<br>

*The platform must allow businesses to link Hey, Blue! to their rewards programs.*

- The platform must be capable of sending requests to external API's (e.g., posting 10 points to the Subway MyWay account associated with a Hey, Blue! user).

  **(7) Interoperability** - Although the intial iteration of the Hey, Blue! platform will not include this feature, the architecture should facilitate its future addition.
