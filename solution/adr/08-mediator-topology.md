# Using the Mediator Topology for our Event-Driven Architecture Solution

## Status
Accepted

## Context
In the _Fundamentals of Software Architecture_ book, the authors Richards and Ford write about the two primary topologies within event-driven architecture. The mediator topology in particular is commonly used when a platform needs control over the workflow of event processes.

## Decision
Workflow is one of our top 3 desired architecture characteristics, which motivated us to adopt the mediator topology for our event-driven architecture.

## Considered Options
The other option for an event-driven architecture is to use the broker topology. On its chapter on event-driven architecture style, the book _Fundamentals of Software_ states that "[t]he broker topology differs from the mediator topology in that there is no central event mediator." Based on our interaction workflow, it would further increase the complexity of its implementation.

## Consequences

### Pros
- Workflow control
- Recoverability
- Restart capabilities
- Better data consistency

### Cons
- Lower scalability
- Lower performance
- Lower fault tolerance
