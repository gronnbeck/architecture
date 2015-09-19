# Architecture

My thoughs on building service oriented architecture

### Databases

Avoid sharing databases between services

![Services sharing databases](imgs/01-database-dont.png)

Try to have one database for each service

![One database per service](imgs/02-database-try.png)

### Coupling

Avoid sharing internal state with external services

![Dont share internal state with external components](imgs/03-coupling-avoid.svg)

Try to expose internal state using external interfaces

![Try to expose internal state using external interfaces](imgs/04-coupling-try.svg)

### Dependencies

Avoid creating unecessary dependencies inside base services

![Avoid creating unecessary dependencies inside services](imgs/05-dependencies-avoid.svg)

Try to manage data relationships in the applications. Duplicating the logic once
or twice is not DRY but it is more flexible
![Avoid creating unecessary dependencies inside services](imgs/06-dependencies-try.svg)

If many applications depens on the same logic create another service unifying the
base services. If need be an application can both be dependent of the base services and
the service aggregate

![Avoid creating unecessary dependencies inside services](imgs/07-dependencies-try2.svg)

### TODO
 * What is what?
  * Hexagon: Microservices
  * Vertical silos: Databases
  * Circles: Applications
 * Sync vs Async
