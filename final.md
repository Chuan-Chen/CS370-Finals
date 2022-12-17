## Final Study Guide CS370
-----

### General Terms for the models below

- User Requirements – User’s perspective (less technical maybe have User Story)
- System Requirements – Actual design from the programmer’s perspective 
- Functional – specifically requested by the user. 
- Non-Functional – Implied by the Functional requirements. Can have greater impact because the system 
- Ethnography – Users may not use the software because it does match the way people work/think. For example, if my subway car has 100 seats only 80 seats might ever be used even if a subway seat is available someone may not want to sit next to someone else in a particular situation.

- The requirements for a system are the descriptions of the services that a system should provide and the constraints on its operation.
The process of finding out, analyzing, documenting
and checking these services and constraints is called requirements engineering (RE).
Functional requirements, as the name suggests, have traditionally focused on
what the system should do.
Even if the software is being re-used there is a need for requirements, in this case, mostly data requirements and also configuration.
Ideally, the functional requirements specification of a system should be both
While it is often possible to identify which system components implement specific
functional requirements (e.g., there may be formatting components that implement
reporting requirements), this is often more difficult with non-functional
requirements. The implementation of these requirements may be spread throughout
the system, for two reasons:

1. Non-functional requirements may affect the overall architecture of a system
rather than the individual components. For example, to ensure that performance
requirements are met in an embedded system, you may have to organize the
system to minimize communications between components.

2. An individual non-functional requirement, such as a security requirement, may
generate several, related functional requirements that define new system services
that are required if the non-functional requirement is to be implemented.
In addition, it may also generate requirements that constrain existing requirements;
for example, it may limit access to information in the system.
Product requirements These requirements specify or constrain the runtime
behavior of the software. Examples include performance requirements for how
fast the system must execute and how much memory it requires; reliability
requirements that set out the acceptable failure rate; security requirements; and
usability requirements.

2. Organizational requirements These requirements are broad system requirements
derived from policies and procedures in the customer’s and developer’s
organizations. Examples include operational process requirements that define
how the system will be used; development process requirements that specify the

programming language; the development environment or process standards to
be used; and environmental requirements that specify the operating environment
of the system.

3. External requirements This broad heading covers all requirements that are
derived from factors external to the system and its development process. These
may include regulatory requirements that set out what must be done for the system
to be approved for use by a regulator, such as a nuclear safety authority;
legislative requirements that must be followed to ensure that the system operates
within the law; and ethical requirements that ensure that the system will be
acceptable to its users and the general public.


- Component testing, where several individual units are integrated to create composite components. Component testing should focus on testing the component
interfaces that provide access to the component functions.
- Interface misuse A calling component calls some other component and makes an
error in the use of its interface. This type of error is common in parameter interfaces,
where parameters may be of the wrong type or be passed in the wrong
order, or the wrong number of parameters may be passed.
- Interface misunderstanding A calling component misunderstands the specification
of the interface of the called component and makes assumptions about its behavior.
The called component does not behave as expected, which then causes unexpected
behavior in the calling component. For example, a binary search method may be
called with a parameter that is an unordered array. The search would then fail.
- Timing errors For example, slow dataset queries will timeout. Solution, quicker queries or change timeout.

- Failure Testing - Where a component is called through a procedural interface, design tests that deliberately cause the component to fail. Differing failure assumptions are one
of the most common specification misunderstandings.
Make sure that code fails when it should fail. For example if you are storing too many items in an array it should crash. Another example, bad code should cause an error from the compiler.

- Stress testing in message passing systems. This means that you should
design tests that generate many more messages than are likely to occur in practice.
This is an effective way of revealing timing problems.
For example, testing a website to see if it can handle all the traffic.

- Shared Memory Testing Where several components interact through shared memory, design tests that vary the order in which these components are activated. These tests may reveal implicit assumptions made by the programmer about the order in which the
shared data is produced and consumed.

- System Testing where some or all of the components in a system are integrated
and the system is tested as a whole. System testing should focus on testing component
interactions.
 Find inputs or input sequences where the behavior of the software is incorrect,
undesirable, or does not conform to its specification. These are caused by defects
(bugs) in the software. When you test software to find defects, you are trying to
root out undesirable system behavior such as system crashes, unwanted interactions
with other systems, incorrect computations, and data corruption.
- Release testing, where a separate testing team tests a complete version of the
system before it is released to users. The aim of release testing is to check that
the system meets the requirements of the system stakeholders.

- Demonstrate to the developer and the customer that the software meets its
requirements. For custom software, this means that there should be at least one
test for every requirement in the requirements document. For generic software
products, it means that there should be tests for all of the system features that
will be included in the product release. You may also test combinations of features
to check for unwanted interactions between them.

Release testing is the process of testing a particular release of a system that is intended
for use outside of the development team. Normally, the system release is for customers
and users. In a complex project, however, the release could be for other teams that are
developing related systems. For software products, the release could be for product
management who then prepare it for sale.
There are two important distinctions between release testing and system testing
during the development process:
1. The system development, team should not be responsible for release testing.
2. Release testing is a process of validation checking to ensure that a system meets
its requirements and is good enough for use by system customers. System testing
by the development team should focus on discovering bugs in the system
(defect testing).
The primary goal of the release testing process is to convince the supplier of the
system that it is good enough for use. If so, it can be released as a product or delivered
to the customer. Release testing, therefore, has to show that the system delivers
its specified functionality, performance, and dependability, and that it does not fail
during normal use.
- Release testing is usually a black-box testing process whereby tests are derived
from the system specification. The system is treated as a black box whose behavior
can only be determined by studying its inputs and the related outputs. Another name
for this is functional testing, so-called because the tester is only concerned with
functionality and not the implementation of the software.
Two ways to do release testing 
    - Requirements-based testing
    - Scenario Testing



User testing/ Acceptance Testing, where users or potential users of a system test the system in their
own environment. For software products, the “user” may be an internal marketing
group that decides if the software can be marketed, released and sold.
Acceptance testing is one type of user testing where the customer formally tests
a system to decide if it should be accepted from the system supplier or if further
development is required.
1. Alpha testing, where a selected group of software users work closely with the
development team to test early releases of the software.
2. Beta testing, where a release of the software is made available to a larger group
of users to allow them to experiment and to raise problems that they discover
with the system developers.
3. Acceptance testing, where customers test a system to decide whether or not it is ready to be accepted from the system developers and deployed in the customer environment

- Testing can only show the presence of errors in a program. It cannot show that there are no remaining faults.
- Development testing is the responsibility of the software development team. A separate team should be responsible for testing a system before it is released to customers. 
In the user testing process, customers or system users provide test data and check that tests are successful.
- Development testing includes unit testing where you test individual objects and methods; component testing in which you test related groups of objects; and system testing in which you test partial or complete systems.
- When testing software, you should try to “break” the software by using experience and
guidelines to choose types of test cases that have been effective in discovering defects in other systems.
- Wherever possible, you should write automated tests. The tests are embedded in a program that can be run every time a change is made to a system.
- Test-first development i( also Test Driven Development) is an approach to development whereby tests are written before the code to be tested. Small code changes are made, and the code is refactored until all tests execute
successfully.
- Scenario testing is useful because it replicates the practical use of the system. It involves inventing a typical usage scenario and using this to derive test cases.
- Acceptance testing is a user testing process in which the aim is to decide if the software is good enough to be deployed and used in its planned operational environment.

Process Models
We will be covering all of Chapter 2 until the end of chapter where Process Improvement is discussed
What is a process model (SDLC)? 
Note: Even if you have no planning that is also a process model (Big Bang Model)
Process Model (Software Development Life Cycle)– Direct how we intend to develop the software
A system how we decide we are going to develop software, i.e. how we are going about the processes of requirements, design, implementation, validation, and evolution (maintenance).



------
### Software Development Models
-----
1. [Waterfall_Model]
    - Requirements
    - Feasiblity
    - Design
    - Development
    - Documentation
    - Release
    - Maintenanace/Evolution

<img src = "https://i.imgur.com/5NTccUX.png">

[Waterfall_Definiton]: The waterfall model is a classical model used in system development life cycle to create a system with a linear and sequential approach. It is termed as waterfall because the model develops systematically from one phase to another in a downward fashion.
If at the end we discover a need to go back to a previous step, then we need to repeat all the steps that are down stream from that step. I.E. If we have to change a feature then we go to the first step and then repeat all the other steps afterwards (for that feature).


[Waterfall_+] Pros
- Simple projects or smaller companies with clear and <b>unchanging requirements </b>
- Embedded systems, Systems that works directly with hardware – expensive to change the hardware when software changes.
- Critical System,regulated (Medical – PaceMaker, DaVincii System FDA approved, Flight FAA, or Car software especially self driving car software NHTSA)
- Distributed Systems (many development groups are working on the same project – any changes will affect all groups)



[Waterfall_-] Cons
- Complex Projects
- Changes in project or even a chance of change does not fit waterfall model
- Developers cannot start on development until the first requirement is met which is "Requirements"
- Client will not see the product until it is completed 

-----
```
Note: Bolded are what he highlights on his reviewsheet but the other are from his image see below.
```
2. Intergration and Configuration model
    - <b>Requirements</b>
        - <b>Software discovery</b>
        - Software evaluation
    - <b>Requirements refinement</b>
        - (Application System Available)<b>Configure</b> application system
        - (Components Available)
            - <b>Adapt Componets</b>, Develop new componets
                - <b>Intergrate System</b>

<img src = "https://i.imgur.com/11r0Txe.png">

[Intergration_Configuration_Definition]: another way of saying re-using software

[Intergration_Configuration_Re-Use]: 
1. Standalone applications. ie ms word
2. Component/libraries
3. Web services

[Intergration_Configuration_+]:
- Saves time and money because the components have been tested, designed and coded.  


[Intergration_Configuration_-]: 
- No Control over code
- Code needs to be licensed since it doesn't belong to you.
- The developer may retire.
------
3. V-Model
<img src = "https://www.scnsoft.com/blog-pictures/custom-software-development/2-v-model-.png">

[V-Model_Definiton]: Create the tests for each level at the same time we design that level
(i.e. architectural tests when designing architecture and feature tests when doing requirements)

[V-Model_+]:
- Very scrict.
- Projects where failures and downtimes are unacceptable. ie medical software, aviation software


[V-Model_-]:
- Will not work well with products that are fluid hard to change


-------
### The following models follow the [agile_manifesto]

- User Stories
    - as a,
    - I want to
    - so that,
    - it is fixed when 
    - ex: “As a [persona], I [want to], [so that].”
As Max, I want to invite my friends, so we can enjoy this service together.
As Sascha, I want to organize my work, so I can feel more in control. 
As a manager, I want to be able to understand my colleagues' progress, so I can better report our success and failures. 

- Refactoring: fixing spaghetti code
- Test Driven Development (TDD) or Unit Tests
- Use Case Diagram/Table
    - Actor – anyone or anything that performs a behavior (who is using the system)
    - Stakeholder – someone or something with vested interests in the behavior of the system under discussion (SUD)
    - Preconditions – what must be true or happen before and after the use case runs.
    - Triggers – this is the event that causes the use case to be initiated.
    - Main success scenarios [Basic Flow] – use case in which nothing goes wrong.
    - Alternative paths [Alternative Flow] – these paths are a variation on the main theme. These exceptions are what happen when things go wrong at the system level
    - Outcome: Result .

<img src = "https://i.imgur.com/08VHLx6.png">

Use actual use case (table) is a detailed view of requirements and 
a user story/scenario is a high-level view.
1. The actor(s): This is the person or group of people interacting with the system. They are the users of the system. For example, an accountant or a CEO or account holder.
2. The goal: This is the outcome for which the use case was designed. It is usually the result of this process. For example, “user logged in” is the goal for Sign On screen.
3. Preconditions: It is the combination of all factors necessary for the case to occur. For example, if a user went to my web site and clicked sign in. Basically, this is where my code will begin.
4. Triggers: What sets the use case in motion. I am notified that a user wishes to Sign In.
5. Main success scenarios [Basic Flow] – use case in which nothing goes wrong. 
Probably include images of what the user should see on the screen.
6. Alternative paths [Alternative Flow] – these paths are a variation on the main theme. These exceptions are what happen when things go wrong at the system level. i.e. user forgot password or password fails 3 times
7. Post Conditions: What will be achieved after my paths. User will be signed in and able to withdraw money.




1. The informality of agile development is incompatible with the legal approach to
contract definition that is commonly used in large companies.
2. Agile methods are most appropriate for new software development rather than
for software maintenance. Yet the majority of software costs in large companies
come from maintaining their existing software systems.
3. Agile methods are designed for small co-located teams, yet much software
development now involves worldwide distributed teams.
4) Code will be unorganized from all the changes
5) Management isn’t clear on the progress of the project because the project is always changing.


User Story – from the perspective of the User.
User Story – As an editor (user) I need to write an essay (action) and save it so I can do my job (result or value statement).
This will be completed when I can write and save my essay (Acceptance Criteria).
1. User Stories Must Always Have a User!
2. User stories capture what the user wants to achieve in a simple sentence
3. User stories contain a qualifying value statement
4. User stories contain acceptance criteria


------

4. Incremental Model
    - Concurrent activties
        - Specification
            - Initial version
        - Development
            - Intermediate version
        - Validation
            - Final version

<img src = "https://i.imgur.com/PG0t772.png">

[Incremental_Definition]: Start with an outline of general requirements
Then we have a loop through the general requirements producing a chunk at a at time.
Each chunk will have a complete requirement, design, implementation, and testing phase.
When the last chunk has been completed project is done.

[Incremental_+]:
- Easy to intergrate because it is structured the way developers think
- changes are easy to make in this model
- Quicker feedback
- Easy delivery, possible to deliver partially completed projects


[Incremental_-]:
- Hard to document
- Spaghetti code, each iteration is adding new fetures
- code needs to be refactored
- Client confused because they don't end up with the finish product.

----

5. SCRUM/Xtream Programming
    - Sprint 1
        - Plan 
            - Design
                - Develop
                    - Test
                        - Deploy working increment
        - Review
    - Sprint 2 (same as sprint 1 takes as long as it needs to product completion)
    - Spring 3

<img src = "https://www.scnsoft.com/blog-pictures/custom-software-development/6-scrum-.png">

[SCRUM_Definition]: product owner/daily meetings(scrum is a meeting)/sprint should take 2 -4 weeks/product backlog/any iteration/sprint can produce a potentially shippable system

[SCRUM_+]:
- Great when end user feedback is required
- Mid-sized projects for where business requirements cannot be directly stated
- Large-sized projects that are easily broken down into smaller parts.


[SCRUM_-]:
- Only works with experianced team members
- chances of project failure is high due to 'no end' in sight

<img src = "https://i.imgur.com/HlntMDa.png">

------
### Diagrams
------

- Sequence diagram
<img src = "https://i.imgur.com/1xBYP16.png">
- Use Case Diagram – Actor and Use Cases (activities)
<img src = "https://i.imgur.com/08VHLx6.png">
- Use Case Table
<img src = "https://i.imgur.com/ntbSl1z.png">>
- State Diagram
<img src = "https://i.imgur.com/iM0SVZ7.png">
- Activity Diagram
<img src = "https://i.imgur.com/mrMIcb1.png">
<img src = "https://i.imgur.com/C99lrDe.png">
- Class Diagram (Inheritance/Composition/aggregation/multiplicity(cardinality)/dependency)
<img src = "https://i.imgur.com/pt4TTBD.png">
- Swim Lanes
<img src = "https://grapholite.com/Images/SwimlaneTemplate.png">
<img src = "https://grapholite.com/Images/SwimlaneTemplate.png">
- Context Diagram
<img src = "https://i.imgur.com/qgrnXrP.png">
- Actor
<img src = "https://sourcemaking.com/files/sm/images/uml/img_20.jpg">
- Starting point/Ending point
<img src = "">
- Transitions/ Transformations
<img src = "">
- Return messages
<img src = "">
- Messages
<img src = "">
- Time
<img src = "">

------
### Design Patterns

What are design patterns and how do they help us?
Design Patterns are designs that were found to be used by programmers to solve existing design issues. We don’t need to reinvent the wheel; someone has a solution already.

Way of communicating with other programmers quickly.

----- 
- Observer Pattern - Without changing code we can add or remove listeners, Open Closed Closed Principle
- Open Closed Principle – open for extension closed for modification
- Strategy – Encapsulate changing behavior in a class. Without changing code or adding inheritance we can change behavior of class, Open Closed Principle, Dependency Injection, Composition over inheritance, Dependency Inversion uses an interface for the behavior.

- Dependency Injection (pass in a database object to the accounting class)
- Favor Composition Over Inheritance – because Inheritance too tightly coupled and therefore restrictive
- Memento - Encapsulate the state of an object in another Object and store it outside the object – Caretaker – keeps history, Originator – Object creating the memento
- Single Responsibility Principle – A class should only do one thing well
- State Pattern - Have an object correspond to a given state
- Encapsulate the code so we don’t change existing code when adding a new state
- Decorator - call other objects in any order without modifying existing code
we dont change existing code when calling another object
- Singleton - One instance of an object 
maybe not thread safe, global object – encapsulate a global objects
- Iterator - hides the concrete collection from outside the class
- Encapsulation - protections data collection using the iterator interface
- Factory - hides the object construction - encapsulation
- Builder Pattern - Fixes issue in many languages that have constructors which have no return value. 

---------
### Testing Types
---------
1. Unit Tests
2. Partition Tests 
3. Guideline base Testing - eg passing null values will usually crash a program
4. Black box testing - Tester has no knowledge of actual code
5. White box testing - Tester has knowledge of actual code
    1. Developer level - class level
    2. component testign - interaction within class/modules
    3. System test - test the whole system
    4. Release Test - anybody but the developer
    5. Acceptance Test - Done by the user to make sure they are happy 

- When you test software, you are trying to do two things:
    - Features -Software performs the way it is supposed to.
    - Defects - Software does not crash. 
Most defects are caused because the developers made certain assumptions regarding how the program will be used that were incorrect.
- TDD advantages (Test Driven Development i.e. Unit Tests)
    - Developer concentrates on the code he/she will develop.
    - The company has a valid test that runs by itself.

```
Five stages of testing: Development testing (unit testing) TDD Test Driven Development, Component testing, System Testing, Release testing, User testing
```
Development testing - where the system is tested during development to discover bugs and defects. System designers and programmers are likely to be involved
in the testing process.

1. Unit testing, where individual program units or object classes are tested. Unit
testing should focus on testing the functionality of objects or methods.
Cheapest impact because once the test is written the test can be run automatically.
2. Partition testing, where you identify groups of inputs that have common characteristics and should be processed in the same way. You should choose tests from
within each of these groups.
    - <img src = "https://i.imgur.com/izS89a3.png">



3. Guideline-based testing, where you use testing guidelines to choose test cases.
These guidelines reflect previous experience of the kinds of errors that programmers
often make when developing components.
Guidelines encapsulate knowledge of what kinds of test cases are effective for discovering errors. 
For example, when you are testing programs with sequences, arrays, or lists,
guidelines that could help reveal defects include:
    1. Test software with sequences that have only a single value. Programmers naturally
think of sequences as made up of several values, and sometimes they
embed this assumption in their programs. Consequently, if presented with a
single-value sequence, a program may not work properly.
    2. Use different sequences of different sizes in different tests. This decreases the
chances that a program with defects will accidentally produce a correct output
because of some accidental characteristics of the input.
    3. Derive tests so that the first, middle, and last elements of the sequence are
accessed. This approach reveals problems at partition boundaries.


--------
### Architectural Pattern
[Architectural_Pattern_Definition]: is a general, reusable solution to a commonly occurring problem in software architecture within a given context. Architectural patterns are similar to software design pattern but have a broader scope.

#### <b>Principles</b>
1. <b>Performance</b> If performance is a critical requirement, the architecture should be
designed to localize critical operations within a small number of components,
with these components deployed on the same computer rather than distributed
across the network. This may mean using a few relatively large components
rather than small, finer-grain components. Using large components reduces the
number of component communications, as most of the interactions between
related system features take place within a component. You may also consider
runtime system organizations that allow the system to be replicated and executed
on different processors.
Also we should minimize database and internet communication because these types of communication are very slow.
E.g. Alexa machine – Only understands the word “Alexa” and then sends your voice to amazon and then amazon will figure out what to do and tells Alexa what to do. So performance is not an issue for Alexa because it is always slow because it works over the internet.
A Tesla cannot use the same model as Alexa because a Tesla would crash before receiving a response from Tesla.

2. <b>Security</b> If security is a critical requirement, a layered structure for the architecture
should be used, with the most critical assets protected in the innermost layers
and a high level of security validation applied to these layers.

3. <b>Safety</b> If safety is a critical requirement, the architecture should be designed so
that safety-related operations are co-located in a single component or in a small
number of components. This reduces the costs and problems of safety validation
and may make it possible to provide related protection systems that can safely
shut down the system in the event of failure.

4. <b>Availability</b> If availability is a critical requirement, the architecture should be
designed to include redundant components so that it is possible to replace and
update components without stopping the system. I describe fault-tolerant system
architectures for high-availability systems in Chapter 11. 
E.g. If a database goes down there is a rollover database to take over, every transaction must be saved in all databases (main data server and the rollover)

5. <b>Maintainability</b> If maintainability is a critical requirement, the system architecture
should be designed using fine-grain, self-contained components that may
readily be changed. Producers of data should be separated from consumers, and
shared data structures should be avoided.


--------
1. Layered Pattern - The most commonly found 3 Layers of a general information system are as follows
    - Presentation layer (UI Layer)
    - Business Logic layer (Domain Layer)
    - Data Access layer (Presistence Layer)

[Usage]:
- General desktop Applications
- E commerece Web Applications

[Benefits]: 
- Easy to swap out one layer with another.
- Natural partition of work


<img src = "https://i.imgur.com/340zOzH.png">

-------
2. Client-Server Pattern - This pattern consist of two parties; a server and multiple client components. The server component will provide services to the multiple client components. Client request servicse from the server and the server provides relevant services to those clients. Furthermore, the server continues to listen to client requests. (Web browser/Web Server, Outlook/Microsoft Exchange
)

[Usage]: 
- Applications such as email, websites, document sharing and banking

[Benefits]: 
- Easy to swap out server or client.
- Can have a thin client
Downside 
- latency (speed)

[Downsides]:
- latency (speed)

<img src = "https://i.imgur.com/Byuqyk0.png">

-------
3. Pipe-filter Pattern - This pattern can be used to structure systems which produce and process a stream of data. Each processing step is enclosed within a filter component. Data to be processed is passed through pipes. These spipes can be used for buffering or for synchronization purposes.

[Usage]:
- Compilers. The consecutive filters perform lexical analysis, parsing, semantic analysis, and code generation.

[Benefits]: 
- Easy to extend

[Downsides]:
- Communicating between processes may be slow. i.e. they may communicate with a file.

<img src = "https://i.imgur.com/D31OzkW.png">

---------

4. Peer-to-peer pattern - In this pattern, individual components are known as peers. Peers may function both as a client request services from other peers, and as a server, prodiving services to other peers. A peer may act as a client or as a server or as both, and it can change its role dynamically with time.

[Usage]: 
- File-sharing networks (GNUTELLA, G2)
- Multimedia protocols (P2PTV, PDTP)
- Cryptocurrency-based products (Bitcoin, blockchain)

[Benefits]: 
- Distributed computing

[Downsides]:
- allowing a program running on your machine that talks directly to other machines isn’t very secure.


<img src = "https://i.imgur.com/YHkj15Y.png">

--------

5. Model-View-Controller Pattern - This pattern, aka MVC pattern, divides an interactive application in to 3 parts.(below) this is done to separate internal representations of the information from the ways information is presented to, and accepted from, the user. It decouples components and allow efficent code reuse. (M = Model (business logic and DB V = View i.e. presentation C=Controller reacts to user input (for websites)- (business logic) view (presentation) -controller (part that controls the model and view))

    1. Model - Contains the core functionality and data
    2. View - displays the info to the user, more than one can be defined
    3. Controller - Handles the input from the user.

[Usage]: 
- Architecture for (WWW) applications in major programming languages
- Web frameworks (Django, Rails)

[Benefits]: 
- similar to layered pattern except both model and view are on same
Controller Model View


[Downsides]:
- introduces complexity and is difficult to debug

<img src = "https://i.imgur.com/NVT0BjZ.png">

------
### OOP (Object Oriented Programming)
------
1. Inheritance
2. Encapsulation (protect data)
3. Polymorphism (different implementations of same method)
4. Abstraction (make the code less complex)

Problems with inheritance only.
1) fragile base class - changing base class breaks the classes
2) Class explosion - if you use inheritance for every type of object
3) because the child class is stuck with all the parent’s code

------
### Misc
------

- SOLID concepts are:
Single-responsibility principle: "There should never be more than one reason for a class to change." In other words, every class should have only one responsibility.[
The Open–closed principle: "Software entities ... should be open for extension but closed for modification."
The Liskov substitution principle: "Functions that use pointers or references to base classes must be able to use objects of derived classes without knowing it."[8] See also design by contract.[8]
Rectangle = Area = L * H Square Area = L * L or H * H if square inherits rectangle then the area formula will not work
The Interface segregation principle: "Multiple specific interfaces are better than one general-purpose interface which cause the children to create unnecessary methods,
The Dependency inversion principle: 
A B C
 
- High-level modules should not import anything from low-level modules. Both should depend on abstractions (e.g., interfaces).
Abstractions should not depend on details. Details (concrete implementations) should depend on abstractions.
 ```
// telling the user their balance
class factory
{
	GetData  getDataReader()
{
		return new ReadTable();
}
}
interface GetData
{
}
class CalculateBalance
{
	// use an interface type
GetData getData = new factory.getDataReader();	
}
 
// reads the database
class ReadTable implements GetData{
	
}
// neither Read Table or CalculateBalance know about each other
// therefore we are using dependency inversion
 ```
- DRY – Don’t repeat yourself - extract common code into a single function
Encapsulate What Changes - code that changes should be seperated
- Favor Composition over Inheritance 
- Programming for Interface not implementation (same as dependency inversion)
You should use interface type on variables, return types of a method or argument type of methods in Java like return Shape object rather than Rectangle object
- Delegation principle- i.e . Draw Method - each object should have its own draw method 
- Parent classes should not do work for their children
Don’t do all stuff by yourself, delegate it to the respective class. Classical example of delegation design principle is equals() and hashCode() method in Java.

------
### Terms
------
- GUI – Graphical User Interface
- Design Pattern
- SCRUM
- Heterogeneity
- Security
- Scalable,
- Dev Ops – continuous integration
- OOP 
- Dependability
- Software Engineering - definition Software projects should be - - - professionally managed and developed
- Different techniques are appropriate for different types of systems. 
- Safety critical control systems require a complete and analyzable specification to be developed.
- Different methods and techniques are needed for different project types
- Computer Science focuses on theory and fundamentals; 
- Software Engineering is concerned with the practicalities of developing and delivering useful software.

Types of applications
1. Stand-alone application
2. Interactive transaction-based applications 
3. Embedded control systems 
4. Batch processing systems 

Design Patterns – decouple code
- Factory Pattern
- Observer
- Singleton Pattern
- State
- builder pattern
 
OOPS
4 basic –
Abstraction
Encapsulation
Polymorphism
Inheritance

- Dependency Inversion
Don’t Repeat Yourself
Single Responsibility Principle
IS-A 

HAS A 
– Composition 2 types Aggregation and Composition
interface segregation principle
Open Closed Principle
Liskov Substitution Principle
SRP
Prefer Composition to inheritance
