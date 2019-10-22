# Combine

### Framework
## Combine
[link](https://developer.apple.com/documentation/combine)

> Customize handling of asynchronous events by combining event-processing

-------------

## Overview

The Combine framework provides a declarative Swift API for processing values overtime. These values can represent many kinds of asynchronous events. Combine declares _publishers_ to expose values that can change over time, and _subscribers_ to receive those values from the publishers.

* The Publisher protocol declares a type that can deliver a sequence of values over time. Publishers have operators to act on the values received from upstream publishers and republish them.
* At the end of a chain of publishers, a Sebscriber acts on elements as it receives them. Publishers only emit values when explicitly requested to do so by subscribers. This puts your subscriber code in control of how fast it receivers events from the publishers it's connected to.

Several Foundation types expose their functionality through pubishers, including Timer, NotificationCenter, and URLSession. Combine also provide a built-in publisher for any property that's compliant with Key-Value Observing.

You can combine the output of multiple publishers and coordinat their interaction. For example, you can subscribe to updates from a text field's publisher, and use the text to perform URL requests. You can then use another publisher to process the responses and use them to update your app.

By adopting Combine, you'll make your code esaier to read and maintain, by centralizing your event-processing code and eliminating troublesome techniques like nested closures and convention-based callbacks.

## Topic

### Essentials

[Receiving and Handling Events with Combine](https://developer.apple.com/documentation/combine/receiving_and_handling_events_with_combine)

### Publishers

`protocol` Publisher

`enum` Publishers

`struct` AnyPublisher

`protocol` ConnectablePublisher

`struct` Published

`protocol` Cancellable

`class` AnyCancellable

### Convenience Publishers

`class` Future

`struct` Just

`struct` Deferred

`struct` Empty

`struct` Fail

`struct` Record

### Subscribers

`protocol` Subscriber

`enum` Subscribers

`struct` AnySubscriber

`protocol` Subscription

`enum` Subscriptions

### Subject

`protocol` Subject

`class` CurrentValueSubject

`class` PassthroughSubject

### Schedulers

### Observable Objects

### Encoders and Decoders

### Debugging Identifiers





