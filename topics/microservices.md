# Caveat

> **DO NOT start building new application as microservices!**

> Micro-\* is largely about separating deployment for big teams.

Focus on building a modular, decoupled, easy to change application first.

When we have semi-stable decoupled modules - and there is a real business need - only then we should think about breaking it into microservices.

The process of breaking down the application into microservices is really nuanced, and to do it right requires a lot of knowledge and experience in managing software architecture.

> This is what happens when you read all those Kubernetes / orchestration / microservices / highscalability blog posts starting about 3 years ago, and come to the realization that you don't have Google-scale problems...

Microservices is more of an organizational structure than a software architecture. Basically you more or less HAVE to do Domain Driven Design to separate 'pieces' of the business between many teams.

As I hear stories about teams using a microservices architecture, I've noticed a common pattern.

-   Almost all the successful microservice stories have started with a monolith that got too big and was broken up
-   Almost all the cases where I've heard of a system that was built as a microservice system from scratch, it has ended up in serious trouble.

This pattern has led many of my colleagues to argue that you shouldn't start a new project with microservices, even if you're sure your application will be big enough to make it worthwhile.

[Martin Fowler](https://martinfowler.com/bliki/MonolithFirst.html)

# Microservices

Developing a single application as a suite of small services, each running its own process and communicating with lightweight mechanisms, often an HTTP resource API.

Think of it like an organs system, where each organ has a purpose, the organs form a system, which form an organism.

```
Microservice > Container > Virtual Machine > Hypervisor > Server > Rack > Datacenter > Cloud
```

The other thing that I'd like to point out is that a microservices architecture is only great when the application becomes too large and complex. A microservices architecture requires more resources as it has some additional overhead. Start with a monolithic first.

A microservice can be a complete application including its own UI, business logic and data. **Usually it's just backend and data.**

Each microservice is a team.

# Misconceptions

-   _Micro services enable our teams to choose the best programming languages and frameworks for their tasks_. - Reality: It's super expensive to do this. Team size and investment are critical inputs.

-   _Code generation is evil_ - What's important is creating a defined schema that is 100% trusted.

-   _The event log must be the source of truth_. - Events are critical parts of an interface. But it's okay for services to be the system of record for their resources.

-   _Developers can maintain no more than 3 services each._ Wrong metric.
