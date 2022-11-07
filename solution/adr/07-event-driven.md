# Using an Event-Driven Architecture

## Status
Accepted

## Context
In the _Software Architecture Pattern_ book, the author Mark Richards writes that the event-driven architecture pattern is a popular distributed asynchronous architecture pattern used to produce highliy scalable applications. He also writes that it is highly scalable and can be used for small applications and as well as large.

## Decision
We decided to adopt the event-driven architecture approach for our strategy to future proof the Hey, Blue! platform and its ability to handle the level of responsiveness and fault-tolerance of any real time service, whether it is with a modest user base during the early day adoption or with a larger one, as it grows in popularity.

## Consequences

### Pros
- Easier deployments
- Performance
- Scalability

### Cons
- Complex to implement
- Lack of atomic transactions for a single business process