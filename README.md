# Exchange vocab

This is separated out from the [OVN vocab](https://github.com/openvocab/ovn), of which it is a component. 

## Why?

We are seeing several organizations that do exchanges, but not production processes. They also sometimes use several different software apps that might want to know about those exchanges. Some of them even conduct different exchanges in different apps! As with all of the other Open Vocab projects, its goal is to help different apps talk to each other by means of a common vocabulary and protocols.

## Who uses this?

[NRP](https://github.com/valnet/valuenetwork) is the source of much of the vocabulary, and continues to refine the model, collaborating with user networks like [Sensorica](http://nrp.sensorica.co). [Holodex](https://github.com/open-app/holodex) is using the [organization aspects of the vocab](https://github.com/openvocab/holodex).

But most of the vocabulary comes from the [Resource-Event-Agent (REA) ontology](http://en.wikipedia.org/wiki/Resources,_events,_agents_(accounting_model)) originated by [Professor William McCarthy of Michigan State University](https://www.msu.edu/~mccarth4/) in 1982, used in many places around the world.

## Overview of Exchanges

This vocabulary looks at exchanges of resources from an independent or neutral viewpoint (not the viewpoint of one of the Agents in the exchange). For example, from one Agent's viewpoint, the exchange may be a Purchase, from the other Agent's viewpoint, it might be a Sale. From the neutral viewpoint, it is an exchange of resources, with usually at least two flows of resources, one from each direction. So for example, the seller might give some goods to the buyer, and the buyer might give some money to the seller. Or in a barter exchange, one agent might give the other some books, and the other agent might compensate with some cookies.

This differs from (for example) the [Good Relations Conceptual Model](http://wiki.goodrelations-vocabulary.org/Documentation/Conceptual_model), which otherwise we like. But it assumes Compensation in the form of money; the compensation itself is not a separate promise; and the actual flow events are not part of the model. (That's not a criticism. Good Relations has different goals, and a more minimal model makes sense for them.)

In the [OVN vocab](https://github.com/openvocab/ovn), we want to track not only the offers and promises, but also the actual flows of resources in networks, in all directions.

![exchanges](https://docs.google.com/drawings/d/1BnVK0J6mJd9OCpqLhJPp59vyutK_Q2ggOJJSyMkNc4o/pub?w=485&h=398)

If exchanges happen between agents in different systems, then a resource transfer needs to be separated into a Give event (might be called a Shipment) in one system and a Take event (might be called a Receipt) in the other system.

If the agents operate in the same logical system, then a resource transfer can just be a transfer - a single event where the resource moves from the Giver to the Take - although the Giver and the Taker will have different views of the same event.

### Exchange protocols

Exchanges may use any of several technical protocols, but the main human-level protocol has been in use for many years. It may be called [Offer-Acceptance](https://en.wikipedia.org/wiki/Offer_and_acceptance) or [Conversation for Action](http://conversationsforaction.com/cfa-playground). It may include several preparation stages for agents who have never exchanged anything before, or it may be really simple if they exchange resources all the time.

### Resource flows

One of the purposes of this vocab is to support resource flows connecting many websites. These flows may be oriented around Processes, Exchanges, or combinations of both. We are breaking out the Processes and Exchanges into their own vocab repositories, but here some overview diagrams.

In general, processes and exchanges alternate in a flow. But in some situations, either the processes or the exchanges are more important, and the other is not worth tracking and can be elided. This Exchange vocab is focused on the situations where the processes are not important.

#### Exchange-oriented flow

![exchange-oriented flow](https://docs.google.com/drawings/d/1og6iUscoFmzHm2zkfhwSU3lp6zHPX2j3BfvTmyfGmww/pub?w=720&h=330)


