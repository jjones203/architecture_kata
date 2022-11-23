# Using an Event-Driven Architecture

## Status
Accepted

## Context
In the O'Reilly report _Software Architecture Patterns_, the author Mark Richards writes that the event-driven architecture pattern is a popular distributed asynchronous architecture pattern used to produce highliy scalable applications.

## Decision
We decided to adopt the event-driven architecture approach to future-proof the Hey, Blue! platform.  This architecture style will allow it to maintain responsiveness and fault-tolerance as it grows in popularity.

## Considered Options
We initially considered the microservices and service-based architectures for their agility. But as we worked through the various characteristics that were important, based on the requirements, we decided to base our solution on an event-driven architecture. As an example, Hey, Blue! interactions are based on a specific protocol that these two architectures would not be adequate since they have a low rating for workflows.

## Consequences

### Pros
- Easier deployments
- Performance
- Scalability

### Cons
- Complex to implement
- Lack of atomic transactions for a single business process
