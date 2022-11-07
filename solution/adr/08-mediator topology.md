# Using the Mediator Topology for our Event-Driven Architecture Solution

## Status
Accepted

## Context
In the _Fundamentals of Software Architecture_ book, the authors Richards and Ford write about the two primary topologies within an event-driven architecture. They describe the mediator topology in particular which is commonly used when a platform needs control over the worflow of event processes.

## Decision
Worflows are one of our top 3 architecture characteristics, which pushed us to adopt our solution and strategy to the mediator topology for an event-driver architecture.

## Consequences

### Pros
- Worflow control
- Recoverability
- Restart capabilities
- Better data consistency

### Cons
- Lower scalability
- Lower performance
- lower fault tolerance