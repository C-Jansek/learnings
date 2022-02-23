---
sidebar_position: 1
---

# Implementing Continuous Delivery for Legacy Code

There are 3 and 1/2 common technical barries to achieve Continuous Delivery in situations where the starting point is an existing legacy application:

- Legacy code
- Manual Testing & Release | Slow, inefficient and error prone
- Poor configuration management | Inabillity to reliably and repeatably reproduce a deployment environment
- Feature driven scheduling

## Legacy code

Definition of legacy code (Micheal C. Feathers):

> Legacy code is code without tests.

Most common problems associated with legacy code:

- _No automated testing_
- _Poor modularity_ | Often a monolith; a complicated, deeply couple, hard to change system
- _Slow build and deploy system_ | Limiting the possibility to build and deploy multiple times per day
- _Data migration_ | Difficult to change the format in which (user) data is stored
- _Old technology_

### Testing legacy code

Difficult to retro-fit automated testing to an existing code base. It takes a strategy to add automated tests, and a strategy to make the legacy code more testable.

#### Adding automated tests

Retro-fitting legacy code bases with unit tests is disruptive and inappropriate. Instead we defend the code in the places where we change it. We write higher level functional tests that highlight the part of the code that should be changed. Refactoring is used to decrease coupling and increase isolation of the piece of code that should be changed. This is done until a point where the code can be extracted and completely replaced (whilst keeping the same functionality) without breaking anything else.

When the code is isolated, we can replace and rewrite it using low level unit tests to evaluate the quality of the changes. This will end up with the structure of the legacy application in place, with small components of well tested code in between.

#### Making the legacy code more testable

Refactoring is one of the key skills that are needed when working in legacy code bases. Refactoring allows making behaviour preserving changes to the code base. This can improve testability, maintainability and understandability of the code.

Tips for refactoring:

1. _Remove clutter_ | Rename to remove comments, delete dead code.
2. _Reduce Cyclomatic Complexity_ | Simplify blocks by extracting methods and naming them accordingly.
3. _Compose methods_ | Build methods that explain themselves through naming.
4. _Remove duplication_ | Extract different modules/classes/services/methods that perform the same actions.
5. _Separate Concerns_ | Extract different concerns into distinct modules/classes/services/methods.
6. _Make tiny changes_
7. _Use refactoring tools in the IDE_

### Increasing modularity

Increase modularity by using the problem domain as a guide. Create splits in the code, improve abstraction around these seams and seperate concerns. Apply the [Boy Scout Rule](https://wiki.c2.com/?BoyScoutRule): leave the code in a better state than you found it.

Change the software tactically: do not change everything in one go. Make small, focussed changes on a bounded context(ToDo: Domain Driven Design). Find out what part of the code is closely coupled and has aligning concerns, change one of these blobs at a time.

### Increase speed

Speed up building and deployment of the software to allow for releasing multiple times a day. This will shorten feedback cycles and in turn increase the speed at which the software improves. Experiment to improve performance, such as paralellizing tasks. Measure and test these experiments.

### Data migration

People that change the structure of the data, are responsible for enabling easy data migrations.

### Old technology

Old technology is not a breaking barrier. Continuous Deployment works with every software, it is separate from the software itself.

## Manual test and release

Automate all regression testing. Adopt Acceptance Test Driven Development for all new work. Automate any testing that is madatory for release. Time spent testing manually otherwise can be used to write more tests for new features.

## Configuration Management

Avoid any manual configuration for environments. Automate Deployment, and thus continuous deployment, requires stable, repeatable environments. Automated testing and deployment drives good configuration management.

As far as possible, all changes to the production environment should be version controlled. This allows us to try-out and rollback any changes to the configuration of the production environment. Version controlling the configuration of the production environment has the same benefits as version controlling the software itself.

## Feature driven scheduling

To optimize delivering of features, scheduling for everyone to be busy is not a good way.

One of the ways to optimize delivery, is to reduce waste in the process. Automating as much as possible is one of the ways in waste is reduced.

Development teams can be viewed as queues. Queuing theory learns that the maximum throughput of a queue is at 60 to 70 percent of its maximum capacity. Loading development teams with more than 70% of its capacity means that the team can not cope with unexpected events.

## Sources

- [Continous Delivery - YouTube](https://youtu.be/Z2c3sGUE2GA)
