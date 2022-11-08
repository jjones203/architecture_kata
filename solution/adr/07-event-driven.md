# Using an Event-Driven Architecture

## Status
Accepted

## Context
In the O'Reilly report _Software Architecture Patterns_, the author Mark Richards writes that the event-driven architecture pattern is a popular distributed asynchronous architecture pattern used to produce highliy scalable applications which can be used for small and large applications.

## Decision
We decided to adopt the event-driven architecture approach to future-proof the Hey, Blue! platform.  This architecture style will allow it to maintain responsiveness and fault-tolerance as it grows in popularity.

## Consequences

### Pros
- Easier deployments
- Performance
- Scalability

### Cons
- Complex to implement
- Lack of atomic transactions for a single business process
