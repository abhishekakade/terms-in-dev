# Terms used in Software Development/Engineering/Web Development

## Terms/Abbreviations/Mnemonics/etc

### API -

**Application Programming Interface.**

An application programming interface (API) is an interface or communication protocol between different parts of a computer program intended to simplify the implementation and maintenance of software.

An API may be for a web-based system, operating system, database system, computer hardware, or software library.

[Wiki](https://en.wikipedia.org/wiki/Application_programming_interface)

### A/B Testing -

A/B testing is a way to compare two versions of a single variable/feature, typically by testing user's response to variant A against variant B, and determining which of the two variants is more effective.

It is a randomized experiment with two variants, A and B. It includes application of statistical hypothesis testing or **"two-sample hypothesis testing"** as used in the field of statistics.

[Wiki](https://en.wikipedia.org/wiki/A/B_testing)

---

### BDD -

**Behaviour Driven Development.**

- Derive examples of various expected behaviors from the system.
- Write a set of behaviours in plain english/natural language/using domain terms to ensure everyone involved in development including the customers can understand it.
- Get the examples ratified with customer from time to time by means of conversations.
- Focus on the customer requirements (examples) throughout the development.
- Use these derived examples as acceptance tests.
- Write code to clear these tests.

BDD is an Agile software development process that emerged from Test Driven Development (TDD). It **encourages collaboration among everyone involved** (developers, QA and non-technical or business participants, etc) in a software project. It **encourages teams to use conversation and concrete examples to formalize a shared understanding of how the application should behave**.

This involves **writing a set of behaviours that the user can expect from the system**. The plain english nature of **Context, Event, Outcomes** format means that the team can focus on describing the behaviours that actually matter to the customer.

BDD uses examples that are written in a readable and understandable natural language to illustrate the behavior of the system for everyone involved in the development. BDD offers more precise guidance on organizing the conversation between developers, testers and domain experts.

[Wiki](https://en.wikipedia.org/wiki/Behavior-driven_development)
[TutorialsPoint](https://www.tutorialspoint.com/behavior_driven_development/behavior_driven_development_quick_guide.htm)
[YouTube - BDD](https://www.youtube.com/watch?v=VS6EEUVZGLE) (length: 4 mins)

---

### TDD -

**Test Driven Development.**

- Write an example as a simple test.
- Watch the test fail.
- Write code to make the test pass.
- Refactor and clean your code.

TDD is a software development process that relies on the repetition of a very short development cycle: requirements are turned into very specific test cases, then the software is improved so that the tests pass.

[Wiki](https://en.wikipedia.org/wiki/Test-driven_development)

---

### DRY -

**Don't Repeat Yourself** is a principle of software development aimed at reducing repetition of software patterns, replacing it with abstractions or using data normalization to avoid redundancy.

The **DRY** principle is stated as "Every piece of knowledge must have a single, unambiguous, authoritative representation within a system". The principle has been formulated by Andy Hunt and Dave Thomas in their book The Pragmatic Programmer. They apply it quite broadly to include "database schemas, test plans, the build system, even documentation". When the DRY principle is applied successfully, a modification of any single element of a system does not require a change in other logically unrelated elements. Additionally, elements that are logically related all change predictably and uniformly, and are thus kept in sync.

[Wiki](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself)

---

### KISS -

**Keep It Simple, Stupid!**

The simpler you keep your projects the easier your life will be when it comes to maintenance.
KISS principle states that most systems work best if they are kept simple rather than made complicated; therefore, simplicity should be a key goal in design, and unnecessary complexity should be avoided.

[Wiki](https://en.wikipedia.org/wiki/KISS_principle)

---

### YAGNI -

**You Aren't Gonna Need It.**

YAGNI is a principle of Extreme Programming (XP) that states a programmer should not add functionality until deemed necessary. XP co-founder Ron Jeffries has written: "Always implement things when you actually need them, never when you just foresee that you need them."

[Wiki](https://en.wikipedia.org/wiki/You_aren%27t_gonna_need_it)

---

### Extreme Programming -

Extreme programming (XP) is a software development methodology which is intended to improve software quality and responsiveness to changing customer requirements. As a type of **Agile** software development, **it advocates frequent "releases" in short development cycles**, which is intended to improve productivity and introduce checkpoints at which new customer requirements can be adopted.

[Wiki](https://en.wikipedia.org/wiki/Extreme_programming)

---

### POSIX -

The **Portable Operating System Interface (POSIX)** is a family of standards specified by the IEEE Computer Society for maintaining compatibility between operating systems. POSIX defines the application programming interface (API), along with command line shells and utility interfaces, for software compatibility with variants of Unix and other operating systems.

[Wiki](https://en.wikipedia.org/wiki/POSIX)
[StackOverflow - Simpler Explanation](https://stackoverflow.com/a/1780614/8326599)

---

### Databases

#### CRUD -

**Create, Read, Update, Delete.**

#### SQL - ACID -

In computer science, **ACID** is a set of properties of **database transactions** intended to guarantee validity even in the event of errors, power failures, etc.

**Example** - A great example of an ACID-compliant transaction is a transfer of funds from one bank account to another.

- **Atomicity**
  Atomicity means that you can guarantee that all of a transaction happens, or none of it does. You can do complex operations as one single unit, all or nothing, and a crash, power failure, error or anything else won't allow you to be in a state in which only some of the related changes have happened.

- **Consistency**
  Consistency means that you guarantee that your data will be consistent; none of the constraints you have on related data will ever be violated. During the database transaction, the RDBMS progresses from one valid state to another. The state is never invalid.

- **Isolation**
  The client's database transaction must occur in isolation from other clients attempting to transact with the RDBMS.

  Isolation means that one transaction cannot read data from another users transaction that is not yet completed. If two transactions are executing concurrently, each one will see the world as if they were executing sequentially, and if one needs to read data that is written by another, it will have to wait until the other is finished.

- **Durability**
  The data operation that was part of the transaction must be reflected in nonvolatile storage (computer memory that can retrieve stored information even when not powered — like a hard disk) and persist after the transaction successfully completes. Transaction failures cannot leave the data in a partially committed state.

  [StackOverflow](https://stackoverflow.com/a/3740307/8326599)

  ***

#### NoSQL - BASE -

The BASE acronym was defined by Eric Brewer, who is also known for formulating the **CAP theorem**.
Example - Data Warehouse.
**Basically Available, Soft state, Eventual consistency.**

**A BASE system gives up on consistency.**

- **Basic Availability** - The database appears to work most of the time. The system is guaranteed to be available for querying by all users (No isolation here).
- **Soft State** - Stores don't have to be write-consistent, nor do different replicas have to be mutually consistent all the time. The values stored in the system may change because of the eventual consistency model, as described in Eventual Consistency.
- **Eventual Consistency** - Indicates that the system will become consistent over time, given that the system doesn't receive input during that time (e.g. lazily at read time). As data is added to the system, the system's state is gradually replicated across all nodes. For example, in Hadoop, when a file is written to the HDFS, the replicas of the data blocks are created in different data nodes after the original data blocks have been written. For the short period before the blocks are replicated, the state of the file system isn't consistent.

[StackOverflow](https://stackoverflow.com/questions/3342497/explanation-of-base-terminology)

---

#### CAP Theorem

No discussion of NoSQL would be complete without mentioning the CAP theorem.
The CAP theorem states that a distributed computer system cannot guarantee all of the following three properties at the same time:

- **Consistency:** Similar to the C in ACID, all nodes in the system would have the same view of the data at any time.

- **Availability:** The system always responds to requests.

- **Partition Tolerance:** The system remains online if network problems occur between system nodes.

The CAP theorem states that in distributed networked systems, architects have to choose two of these three guarantees — you can't promise your users all three. That leaves you with the three possibilities shown:

- **Systems using traditional relational technologies normally aren't partition tolerant, so they can guarantee consistency and availability**. In short, if one part of these traditional relational technologies systems is offline, the whole system is offline.

- **Systems where partition tolerance and availability are of primary importance can't guarantee consistency**, because updates (that destroyer of consistency) can be made on either side of the partition. The key-value stores Dynamo and CouchDB and the column-family store Cassandra are popular examples of partition tolerant/availability (PA) systems.

- **Systems where partition tolerance and consistency are of primary importance can't guarantee availability** because the systems return errors until the partitioned state is resolved.

[Source](https://www.dummies.com/programming/big-data/hadoop/acid-versus-base-data-stores/)

---

### SOAP -

**Simple Object Access Protocol.** It is an XML-based messaging protocol for exchanging information among computers. SOAP is an application of the XML specification.

[Wiki](https://en.wikipedia.org/wiki/SOAP)

### REST -

**Representational State Transfer** is a software architectural style that defines a set of constraints to be used for creating Web services. Web services that conform to the REST architectural style, called RESTful Web services, **provide interoperability between computer systems on the Internet**. RESTful Web services allow the requesting systems to access and manipulate textual representations of Web resources by using a uniform and predefined set of stateless operations.

[Wiki](https://en.wikipedia.org/wiki/Representational_state_transfer)

---

### RPC - 

**Remote Procedure Call (RPC)** is a protocol that one program can use to request a service from a program located in another computer on a network without having to understand the network's details. RPC is coded as if it were a normal (local) procedure call, without the programmer explicitly coding the details for the remote interaction. That is, the programmer writes essentially the same code whether the subroutine is local to the executing program, or remote. A procedure call is also sometimes known as a function call or a subroutine call.

This is a form of client–server interaction (caller is client, executor is server), typically implemented via a request–response message-passing system.

[Source](https://searchapparchitecture.techtarget.com/definition/Remote-Procedure-Call-RPC)
[Wiki](https://en.wikipedia.org/wiki/Remote_procedure_call)

---

### Separation of Concerns

The Pragmatic Programmer, one of the best books ever written on Software Engineering, uses the following three terms when talking about **"Separation of Concerns": Orthogonality, Cohesion and Coupling.**

#### Orthogonality

Orthogonality is the idea that modules should be written in a way that a change in one module should not require changes in any other module.

#### Cohesion

Cohesion is a measure of how well the internal contents of a module relate to each other. A cohesive module is one with a single well defined purpose, where all code in the module is related to that purpose. A less cohesive module might have multiple purposes, with pieces of code that are completely unrelated to each other.

#### Coupling

Coupling is a measure of how dependent different modules are on the internal workings of other modules. In a loosely coupled system, any module can be completely rewritten as long as it exposes the same public interface, without any other modules needing to change. In a tightly coupled system, changing the internal details of one module may require changes in many other modules.

---

### Object Oriented Programming (OOP)

#### SOLID -

This is a mnemonic for -

- **Single Responsibility**
  A class should only have a single responsibility, that is, only changes to one part of the software's specification should be able to affect the specification of the class.

- **Open–Closed**
  Software entities (classes, modules, functions, etc.) should be open for extension, but closed for modification.

- **Liskov Substitution**
  Objects in a program should be replaceable with instances of their subtypes without altering the correctness of that program.

- **Interface Segregation**
  Many client-specific interfaces are better than one general-purpose interface.

- **Dependency Inversion**
  High-level modules should not depend on low-level modules. Both should depend on abstractions (e.g. interfaces).
  Abstractions should not depend on details. Details (concrete implementations) should depend on abstractions.

[Wiki](https://en.wikipedia.org/wiki/SOLID)

---

#### The Law of Demeter (LoD)/Principle of least knowledge

It is a design guideline for developing software, particularly **object-oriented** programs. In its general form, the LoD is a specific case of **loose coupling**. It can be summarized in following ways:

- Each unit should have only limited knowledge about other units: only units "closely" related to the current unit.
- Each unit should only talk to its friends; don't talk to strangers.
- Only talk to your immediate friends.

The fundamental notion is that a given object should assume as little as possible about the structure or properties of anything else (including its subcomponents), in accordance with the principle of "information hiding" or **abstraction**. It may be viewed as a corollary to the **principle of least privilege**, which dictates that a module possess only the information and resources necessary for its legitimate purpose.

---

#### Tell, Don't Ask! (TDA Principle) -

This principle tells that we should not ask objects about their state, make decision and only then tell them what to do. Rather we should send commands. Send commands to objects and you will get clean code which is easy to maintain and flexible enough to add new features.

---

#### Facade Pattern -

Analogous to a facade in architecture, a facade is an object that serves as a front-facing interface masking more complex underlying or structural code. This pattern hides the complexities of the larger system and provides a simpler interface to the client. It typically involves a single wrapper class that contains a set of members required by the client. These members access the system on behalf of the facade client and hide the implementation details.

A facade can:

- Improve readability and usability of a software library by masking interaction with more complex components behind a single (and often simplified) API.

- Provide a context-specific interface to more generic functionality (complete with context-specific input validation).

- Serve as a launching point for a broader refactor of monolithic or tightly coupled systems **in favor of more loosely coupled code**.

[Wiki](https://en.wikipedia.org/wiki/Facade_pattern)

---

#### Loose Coupling -

In computing and systems design, a loosely coupled system is one in which each of its components has, or makes use of, little or no knowledge of the definitions of other separate components.

It can be achieved by **Single Responsibility Principle** (SRP) & **Separation of Concerns**.
Makes system more extendable because components aren't dependent on each other and hence there are less chances of code breaking and bugs.

Loose Coupling is good and Tight Coupling should be avoided.

The Law of Demeter, TDA Principle, Facade Pattern all help achieve Loose Coupling.

#### Tight Coupling -

Tight coupling is when a group of classes are dependent on one another.

---

### CQRS -

**Command Query Responsibility Segregation.** **Command/Query Separation** is a principle of imperative computer programming. It was devised by Bertrand Meyer as part of his pioneering work on the Eiffel programming language. It states that every method should either be a command that performs an action, or a query that returns data to the caller, but not both.

---

### Coroutines -

Coroutines are computer program components that generalize subroutines for non-preemptive multitasking, by allowing execution to be suspended and resumed. Coroutines are well-suited for implementing familiar program components such as cooperative tasks, exceptions, event loops, iterators, infinite lists and pipes.

- **Subroutines -**
  In computer programming, a subroutine is a sequence of program instructions that performs a specific task, packaged as a unit. This unit can then be used in programs wherever that particular task should be performed.

  Subroutines may be defined within programs, or separately in libraries that can be used by many programs. In different programming languages, a subroutine may be called a procedure, a function, a routine, a method, or a subprogram. The generic term callable unit is sometimes used.

  Subroutines are special cases of coroutines. When subroutines are invoked, execution begins at the start, and once a subroutine exits, it is finished; an instance of a subroutine only returns once, and does not hold state between invocations. By contrast, coroutines can exit by calling other coroutines, which may later return to the point where they were invoked in the original coroutine; from the coroutine's point of view, it is not exiting but calling another coroutine. Thus, a coroutine instance holds state, and varies between invocations; there can be multiple instances of a given coroutine at once.

  [Wiki](https://en.wikipedia.org/wiki/Subroutine)

[Wiki](https://en.wikipedia.org/wiki/Coroutine)

---

### Asynchronous Programming

Asynchronous Programming is a means of parallel programming in which a unit of work runs separately from the main application thread and notifies the calling thread of its completion, failure or progress.

In a **synchronous programming** model, things happen one at a time. When you call a function that performs a long-running action, it returns only when the action has finished and it can return the result. This stops your program for the time the action takes.

An **asynchronous model** allows multiple things to happen at the same time. When you start an async action, your program continues to run without waiting for the async action to complete. When the action finishes, the program is informed and gets access to the result of that async action (for example, the data read from disk).

At a high level, **asynchronous is the ability to do something while waiting for something else to complete**, and **concurrency is the ability to compute multiple things at the same time**, the big trade off versus **sequential/synchronus** execution being that both asynchronous and concurrent programming add additional complexity.

[Wiki](<https://en.wikipedia.org/wiki/Asynchrony_(computer_programming)>)
[EloquentJavaScript](https://eloquentjavascript.net/11_async.html)

---

### Parallelism -

Parallel computing is a type of computation in which many calculations or the execution of processes are carried out simultaneously. Large problems can often be divided into smaller ones, which can then be solved at the same time. There are several different forms of parallel computing: bit-level, instruction-level, data, and task parallelism.

[Wiki](https://en.wikipedia.org/wiki/Parallel_computing)
[Wiki - Parallel Programming Model](https://en.wikipedia.org/wiki/Parallel_programming_model)

---

### Concurrency -

Concurrency is the ability of different parts or units of a program, algorithm, or problem to be executed out-of-order or in partial order, without affecting the final outcome. This allows for parallel execution of the concurrent units, which can significantly improve overall speed of the execution in multi-processor and multi-core systems. In more technical terms, concurrency refers to the decomposability property of a program, algorithm, or problem into order-independent or partially-ordered components or units.

[Wiki](<https://en.wikipedia.org/wiki/Concurrency_(computer_science)>)

---

## Differences between Machine Code, Bytecode, Object code and Source Code

**Machine code** is code that is directly executable by the computer’s physical processor without further translation. Load into memory and go.

**Bytecode** is code that can be executed by a virtual machine. The virtual machine implementation reads the bytecode and performs the operations it specifies within a virtual environment. Byte code is typically slower than machine code but is portable across platforms: the same byte code will run on any computer for which there is a compatible virtual machine implementation, without regard to the actual physical processor.

**Object code** is code generated by a compiler or other translator, consisting of machine code, byte code, or possibly both, combined with additional metadata that will enable a linker, loader, or linker-loader to assemble it with other object code modules into executable machine code or byte code. Traditionally, a translator that translates source code represented in assembly language is called an “assembler” rather than a compiler, but the same function is being performed. Note that some compilers generate output that is not object code: a compiler might instead translate its input into an intermediate language (such as LLVM IR) or even into a different source code language: many compilers emit code in C, and there are also many compilers that can generate output code in Javascript.

**Source code** is the input to a compiler or other code translator. Source code is normally generated by humans (and thus hopefully able to be read and modified by humans), and is the human-readable representation from which all the other forms of code are created. Note, however, that some languages that are nominally “source” languages are more often generated by computer programs. Javascript, as mentioned previously, is one example; an even more extreme example is the printer-command language Postscript, which was originally designed to be human-readable but in practice almost never is. Virtually all Postscript code generated today is generated by software, intended to be read only by a printer (or, more likely, by a software renderer for display on a screen).

-Answer by Kelly Kinkade.

[Quora](https://qr.ae/TLomMU)

## Terms mostly seen in Web Development

### PWA -

**Progressive Web App.**

### SSO -

**Server Side Optimisation.**

### CSR -

**What is Client Side Rendering?**

With a client-side rendering solution, when the user opens a website, his browser makes a request to the server, and the user gets a response with a single HTML file without any content, loading screen, etc. It is a blank page until the browser fetches all linked JavaScript files and lets the browser compile everything before rendering the content. - [Source](https://altalogy.com/blog/client-side-rendering-vs-server-side-rendering/)

### SSR -

**What is Server Side Rendering?**

Server-side rendering pre-populates a web page with custom user data directly on the server. It renders all the JavaScript on the server rather than on clients browser, which makes it fast at the cost of load on the server and more bandwidth consumption. It is generally faster to make all the requests within a server than making extra browser-to-server round-trips for them. - [Source](https://www.toptal.com/front-end/client-side-vs-server-side-pre-rendering)

### PRPL Pattern -

Push - Render - Pre-cache - Lazy-load.

- Push (or preload) the most important resources.
- Render the initial route as soon as possible.
- Pre-cache remaining assets.
- Lazy load other routes and non-critical assets.

[Source](https://web.dev/apply-instant-loading-with-prpl/)

### RAIL Model -

Response - Animation - Idle - Load.

RAIL is a user-centric performance model that breaks down the user's experience into key actions.

[Source](https://developers.google.com/web/fundamentals/performance/rail)

### Accessibility/a11y -

#### WCAG - POUR -

Web Content Accessibility Guidelines -

- Perceivable
- Operable
- Understandable
- Robust

[WCAG Checklist](https://webaim.org/standards/wcag/checklist)

#### ARIA -

**Accessible Rich Internet Applications**: sometimes also used as **WAI-ARIA**.

---

### AMP -

**Accelerated Mobile Pages**: a mobile web standard initiated by Google with the purpose of making mobile sites faster.

---

### WYSIWYG -

What You See Is What You Get: A type of content editor that allows users to edit text, images, and other content types without writing any markup.

In a WYSIWYG editor, users can see how the end result will look like while they create the content. The post editor interface of WordPress and most blogging platforms are good examples of WYSIWYG systems.

---

### MVC

**Model-View-Controller**: An architectural pattern used in object-oriented programming.

The MVC pattern keeps the data logic separate from the user interface by grouping objects into three groups: Model Objects for the underlying data structure and logic, View Objects for the user interface, and Controller Objects for acting as intermediary between other objects and for task coordination.

---

### CORS

**Cross-Origin Resource Sharing**: Cross-origin resource sharing **(CORS)** is **a mechanism that allows restricted resources (e.g. fonts) on a web page to be requested from another domain outside the domain from which the first resource was served**. A web page may freely embed cross-origin images, stylesheets, scripts, iframes, and videos. Certain "cross-domain" requests, notably `Ajax` requests, are **forbidden by default by the same-origin security policy**.

[Wiki](https://en.wikipedia.org/wiki/Cross-origin_resource_sharing)
[MDN](https://developer.mozilla.org/en-US/docs/Glossary/CORS)

---

### Same-Origin Policy (SOP)

**Same-Origin Policy**: In computing, the same-origin policy (sometimes abbreviated as **SOP**) is an important concept in the web application security model. Under the policy, a **web browser permits scripts contained in a first web page to access data in a second web page, but only if both web pages have the same origin**. An origin is defined as a combination of URI scheme, host name, and port number. This policy prevents a malicious script on one page from obtaining access to sensitive data on another web page through that page's Document Object Model.

[Wiki](https://en.wikipedia.org/wiki/Same-origin_policy)
[MDN](https://developer.mozilla.org/en-US/docs/Web/Security/Same-origin_policy)

---
