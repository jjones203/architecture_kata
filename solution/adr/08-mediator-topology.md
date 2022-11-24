# Using the Mediator Topology for our Event-Driven Architecture Solution

## Status
Accepted

## Context
In the _Fundamentals of Software Architecture_ book, the authors Richards and Ford write about the two primary topologies within event-driven architecture: mediator and broker. Since the mediator coordinates the steps required to respond to a particular event, the mediator topology is commonly used when a platform needs control over the workflow of event processes. The broker topology allows for greater responsiveness but less control over the sequencing of event processes.

## Decision Drivers
- Given our decision to use event-driven architecture, which topology is more appropriate? Are we willing trade greater responsiveness for less workflow control or vice versa?

## Decision
For safety and privacy reasons, the Hey, Blue! platform will require certain events occur in a particular sequence: e.g., a civilian must initiate an interaction, then an officer must accept the chat request. The mediator topology better lends itself to such workflow orchestration.

## Considered Options
The other option for an event-driven architecture is to use the broker topology. On its chapter on event-driven architecture style, the book _Fundamentals of Software_ states, "The broker topology differs from the mediator topology in that there is no central event mediator." We believe this would further increase the complexity of implementing our proposed interaction workflow.

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
