# Using the Mediator Topology for our Event-Driven Architecture Solution

## Status
Accepted

## Context
In the _Fundamentals of Software Architecture_ book, the authors Richards and Ford write about the two primary topologies within event-driven architecture. They mediator topology in particular is commonly used when a platform needs control over the workflow of event processes.

## Decision
Workflow is one of our top 3 architecture characteristics, which motivated us to adopt our solution and strategy to the mediator topology for an event-driven architecture.

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
