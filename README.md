# Reactive Programming.

The term "Reactive" is getting a bit overloaded in the IT community.

There's several reactive paradigms out there that we need to clarify.

## "Reactive"

	1. Reactive System --> Architecture and Design, ie Cloud Native, cloud based application , application large scale, self healing system like google, amazon. 

	2. Reactive Programmer --> It's focused on event based, it's asynchronous non-blocking programming techniques, focused on handling and event, and that event would probably wiil be within a reactive system.

	3. Functional Reactive Programming.(FRP) --> IE Java 8 with functional libraries.


## Reactive Manifesto.

The Reactive Manifesto have 4 conceptos

	1. Elastic. 

	2. Responsive.

	3. Message Driven.

	4. Resilient. 

## Elastic

	1. The system stays responsive under varying workload.

	2. Reactive Systems can react to changes in the input rate by increasing or decreasing resource allocated to service inputs.

	3. Reactive systems achieve elasticity in a cost effective way on commodity hardware and software platforms.

## Responsive.

	1. The system responds in a timely manner.

	2. Responsiveness is the cornerstone of usability and utility.

	3. Responsiveness also means problems may be detected quickly and dealt with effectively.

	4. Responsive systems provide rapid and consistent response times.

	5. Consistent behavior simplifies error handling, builds end user confidence, and encourages further interaction

## Message Driven

	1. Reactive systems rely on asynchronous message passing to establish a boundary between components. --> this ensures loose coupling, isolation andlocation transparency.

	2. Message passing enables load management, elasticity, and flow control.

	3. Location transparent messaging makes management of failure posible.

	4. Non-blocking communications allows recipients to only consume resources while active, leading to less system overhead.

## Resilient

	1. System stays responsive in the face of failure.

	2.  Resilience is achieved by replication, containment, isolation and delegation.

	3. Failures are contained within each component.

	4. Parts of the system can fail, without compromising the system as a whole.

	5. Recovery of each component is delegated to another.

	6. High-availability is ensured by replication where necessary.


## Reactive Programming  with Reactive Systems

	1. Reactive programming is a useful implementation technique.

	2. Reactive programming focuses on non-blocking asynchronous executions - a key characteristics of reactive Systems.

	3. Reactive progrmamming is just one tool in building Reactive Systems.


Reactive Programming is an asynchronous programmin paradimg focused on streams of data.

Reactive programs also maintain a continuous interaction with their environment, but at a speed which is determited by the environment, not the program itself. Interactive programs work at their own pace and mostly deal with communication, while reactive programs only work in response to external demand and mostly deal with accurate interrupt handling. Real-time programs are usually reactive.

## Features of Reactive Programming.

	1. Data Streams

	2. Asynchronous.

	3. Non-blocking.

	4. Backpressure.

	5. Failures as Messages.


## Data Streams

	1. Data Streams can be just about anything.

	2. Mouse click, or other user interactions

	3. JMS Messages, Restful Services calls, twiter feed, stock trades, list of Data from Database.

	4. A Stream is a sequence of events ordered in time.

	5. Events you want to listen to.


## Asynchronous 

	1. Events are captured asynchronous.

	2. A function is defined to execute when an event is emitted.

	3. Another function is defined if an error is emitted.

	4. Another function is defined when complete is emitted.

## Non- Blocking

	1. In blocking, the code will stop and wait for more data(ie reading from disk, network, etc).

	2. Non-blocking in constrast, will process available data, ask to be notified when more is available, then continue.

	3. When you're non-blocking that task or that thread is going to go on to something else.

## Back Pressure.

	1. The ability of the subscriber to throttle data.

## Failures as Messages

	1. Exceptions are not thrown in traditional sense.

	2. Excepcion are processed by a handler function.	

## Commun Uses Case

	1. External Service Call

	2. Highly concurrent message Consumer.

	3. Spreadsheet.

	4. Abstraction Over Asynchronous Processing.

# Reactive Streams 

	1. Goal is to create a standard for asynchronous stram processing with non-blocking back pressure.

	2. Reactive Streams is a set of 4 interfaces which define the API.

## Spring WebFlux 

The normal spring framework is blocking for this reason spring webflux was designed, spring staff created a new full stack inside of spring  called spring Webflux

	1. @Controller / RequestMapping --> Router Functions
	2. spring-webmvc 				--> spring-webflux
	3. Servlet APi 					--> HTTP / Reactive Program.
	4. Servlet container 			--> Tomcat, Jetty, Netty


## Spring Reactives Types

	1. Mono is a publiusher with zero or one elements in data stream.

	2. Flux is a publiser with zero or many elements in data stream.	

