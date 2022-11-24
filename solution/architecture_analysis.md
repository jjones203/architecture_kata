# Architecture Analysis

## Desired Architecture Characteristics
Here we map technical requirements to associated architecture characteristics, which are ordered by importance. This analysis (inspired by the [worksheet](https://www.developertoarchitect.com/downloads/architecture-characteristics-worksheet.pdf)) takes the following format:

*Business requirement*

- Technical capability required of platform

  **Architecture Characteristic**

---

*The platform must facilitate interactions between civilians and officers: in-person interactions when users are near one another or virtual interactions when officers are unavailable for in-person connection. Civilians can find officers that are willing to connect, but officers cannot find civilians.*
- The platform must track users' availability and locations.
- The platform must enable synchronous communication so users can arrange to meet in-person or connect virtually.

  **(1) Availability** - The platform must allow users to connect with each other at any time of day or night. Frequent outages could discourage use of the platform and prevent Hey, Blue! from building a user base. We will aim for 99.9% uptime.

  **(2) Responsiveness** - The platform must handle requests quickly enough to facilitate chats between users. We will aim for most typical user requests to take 0.1-0.2 seconds from the user initiating the request to the app responding to the request, with an outside limit of 1 second for more complex transactions. (See [Designing for Performance](https://designingforperformance.com/performance-is-ux/) for information on users' perception of responsiveness.)

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


## Architecture Style

We evaluated potential architecture styles in light of the analysis above. The architecture styles worksheet showed event-driven architectures exhibit several of the characteristics most important for the Hey, Blue! platform.

![architecture worksheet with the performance, scalability, and workflow characteristics and event-driven style selected](/assets/arch_worksheet_completed_crop.png)

Since the Hey, Blue! platform will share some functionality (e.g., live chat with other users) with social media apps, similar design choices made by several social media platforms reinforced our selection of this style. For example, WhatsApp, Telegram, and Discord are all at least partially implemented in [Elixir](https://hashnode.com/post/learn-elixir-the-language-behind-whatsapptelegram-discord-and-pinterest-ckqb42vqc04r948s146gi9pca). The Elixir language uses [the actor model](https://courses.cs.ut.ee/MTAT.08.024/2020_spring/uploads/Main/B96281_5867_1.pdf), a concurrency framework that relies on messages passed between actors and resembles the event-drive style.

### Feasibility

We believe our solution is feasible as long as the customer understands not only the benefits of such an architecture, but also its caveats. Implementing our solution will require a more experienced team which would be more expensive to hire. As mentioned above, a technology stack using Elixir will satisfy the scalability and concurrency charateristics we are looking for in our architecture. And since it is also based on the Erlang VM, it features seamless updates with no to little downtime, satisfying our availability architecture characteristic. For more information, see their [website](https://elixir-lang.org).

Hardware costs should be minimal, initially. As the Hey, Blue! platform grows in popularity and more concurrent users start using the service, an increase in the hardware specifications should only be necessary to sustain the increased load, without having to update the code nor its architecture. We would like to note that there will need to be a baseline hardware requirement deduced to be able to maintain the desired level of responsiveness and process the geolocation data and compute distances among the logged-in users.
