# Requirement Analysis
Mapping technical requirements to non-functional requirements; this analysis takes the following format:

*Business requirement*

- Technical capability required of platform

**NFR**

1. *The platform must facilitate interactions between civilians and officers: in-person interactions when users are near one another or virtual interactions when officers are unavailable for in-person connection. Civilians can find officers that are willing to connect, but officers cannot find civilians.*
  - Platform must track users' availability and locations. 
  - Platform must enable synchronous communication so users can arrange to meet in-person or connect virtually.

**Responsiveness** - The platform must handle requests quickly enough to facilitate chats between users. We will aim for most typical user requests to take 0.1-0.2 milliseconds from the user initiating the request to the app responding to the request, with an outside limit of 1 second for more complex transactions. 

**Workflow** - For safety and privacy reasons, the platform will only connect users after both parties accept the connection request, which must be initiated by the civilian. The platform must ensure requests and responses occur in the correct order.



