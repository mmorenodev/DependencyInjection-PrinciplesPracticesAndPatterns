# DependencyInjection-PrinciplesPracticesAndPatterns
Learning about Dependency Injection

Dependency Injection is one of the most misunderstood concepts of object-oriented programming. The confusion is abundant and spans terminology, purpose, and mechanics. 
- Should it be called Dependency Injection, Dependency Inversion, Inversion of Control, or even Third-Party Connect? 
- Is the purpose of DI only to support unit testing, or is there a broader purpose?
- Is DI the same as SERVICE LOCATION? 
- Do we need DI CONTAINERS to apply DI?

One of the underlying reasons behind all the inconsistency and bad advice is that the boundaries of DI are quite blurry. Where does DI end, and where do other object-oriented concepts begin? We think that it's impossible to draw a distinct line between DI and other aspects of writing good object-oriented code. 

To talk about DI, we have to pull in other concepts as SOLID, Clean Code, and even ASPECT-ORIENTED PROGRAMMING. We can't credibly talk about DI without also touching on some of these other topics. 

DI CONTAINER: It's entirely possible to apply DI without using a DI CONTAINER. A DI CONTAINER is a helpful, but optional, tool. DI is a container-agnostic topic. 

## Dependency Injection Definition
Dependency Injection IS A SET OF SOFTWARE PRINCIPLES AND PATTERNS THAT ENABLES YOU TO DEVELOP LOOSELY COUPLED CODE. 

## Writing Maintainable code
What purpose does DI serve? DI isn't a goal in itself; rather, it's a means to and end. Ultimately, the purpose of most programming techniques is to deliver working software as efficiently as possible. One aspect of that is to write maintainable code. 
Unless you only write prototypes, or applications that never make it past their first release, you find yourself maintaining and extending existing code bases. To work effectively with such code bases, in general, the more maintainable they are, the better. 
An excellent way to make code more maintainable is through LOOSE COUPLING. As far back as 1994, when the Gang of Four wrote DESIGN PATTERNS, this was already a common knowledge:
'Program to an interface, not an implementation'
This important piece of advice isn't the conclusion, but, rather, the premise of 'Design Patterns'. Loose coupling makes code extensible, and extensibility makes it maintainable. DI is nothing more than a technique that enables loose coupling. Moreover, there are many misconceptions about DI, and sometimes they get in the way of proper understanding. Before you can learn, you must UNLEARN what (you think) you already know. 

## Unit Testing
Some people think that DI is only relevant for supporting unit testing. This isn't true, either, although DI is certiainly an important part of support for unit testing. 

## An Abstract Factory On Steroids
Perhaps the most dangeerous fallacy is that DI involves some sort of general-purpose Abstract FActory that you can use to create instances of the DEPENDENCIES needed in your applicacions. 

Abstract Factory -> This is typically an ABSTRACTION that contains multiple methods, where each method allows the creation of an object of a certain kind. 

Many developers and architects think about DI as a service that can be used to locate other services. This is called a SERVICE LOCATOR, but it's the exact opposite of DI. 
A SERVICE LOCATOR is often called an Abstract Factory on steroids because, compared to a normal Abstract Factory, the list of resolvable types is unspecified and possible endless. 

## DI CONTAINERS
Closely associated with the previous misconception is the notion that DI requires a DI CONTAINER. If you held the previous, mistaken belief that DI involves a SERVICE LOCATOR, then it's easy to conclude that a DI CONTAINER can take on the responsibility of the SERVICE LOCATOR. This might be the case, but its not all how you should use a DI CONTAINER. 
A DI CONTAINER is an 'optional' library that makes it easier to compose classes when you wire up an application, but it's in no way required. When you compose applications without a DI CONTAINER, it's called PURE DI. It might take a little more work, but other than that, you don't have to compromise on any DI principles. 

## Understandig the purpose of DI
DI isn't and end goal it's a means to an end. DI enables loose coupling, and loose coupling makes code more maintainable.

## Checking into a cheap hotel
If you're staying at a cheap hotel, you might encounter a sight like the one in the next figure. Here, the hotel has kindly provided a hair dryer for your convenience, but apparently they don't trust you to leave the hair dryer for the next guest: the appliance is directly attached to the wall outlet. The hotel management decided that the cost of replacing stolen hair dryers is high enough to justify what's otherwise an obviously inferior implementation. 

<img width="487" alt="image" src="https://user-images.githubusercontent.com/66931789/187051110-fb62a300-63f1-4620-8892-d5bb7aeee5c8.png">

What happens when the hair dryer stops working? The hotel has to call in a skilled professional. To fix the hardwired hair dryer, the power to the room will have to be cut, rendering it temporarily useless. Then, the technician must use special tools to disconnect the hair dryer and replace ti with a new one. If you're lucky, the technician will remember to turn the power on to the room back on and go back to test whether the new hair dryer works -if you're lucky. Does this procedure sound at all familiar? 
This is how you would approach working with tightly coupled code. In this scenario, the hair dryer is tightly coupled to the wall, and you can't easily modify one without impacting the other. 

## Comparing Electrical Wiring to Design Patterns
Usually , we don't wire electrical applicances together by attaching the cable directly to the wall. Instead, we use plugs and sockets. A socket DEFINES A SHAPE THAT THE PLUG MUST MATCH.

In an analogy to software design, the socket is an interface, and the plug with its appliance is an implementation. This means that the room (the application) has one or (hopefully) more sockets, and the users of the room (the developers) can plug in appliances as they please, potentially even a customer-supplied hair dryer. 

<img width="697" alt="image" src="https://user-images.githubusercontent.com/66931789/187051248-c29c2692-8223-4cfb-9a6d-f7f998aed6a2.png">

In contrast to the hardwired hair dryer, plugs and socks define a loosely coupled model for connecting electrical appliances. As long as the plug (the implementation) fits into the socket (implements the interface), and it can handle the amount of volts and hertz (obeys the interface contract), we can combine appliances in a variety of ways, What's particularly interesting is that many of these common combinations can be compared to well-known software design principles and patterns. 

## Liskov Substitution Principle
It's amazing that the concept of a socket predates computers by decades, and yet it provides an essential service to computers. The original designers of sockets couldn't possibly have foreseen personal computers, but because the design is so versatile, needs that were originally unanticipated can be met. 

The ability to switch plugs, or implementations, without requiring a change to the socket, or interface, is similar to a central software design principle called the LISKOV SUBSTITUTION PRINCIPLE. This principle states that we should be able to replace one implementation of an interface with another without breaking either the client or the implementation. 
When it comes to DI, the LISKOV SUBSTITUTION PRINCIPLE is one of the most important software design principles. It's this principle that enables us to address requirements that occur in the future, even if we can't foresee them today. 

There are many other things you can do, as well. If you live in a neighborhood with intermittent power failures, you may want to keep the computer running by plugging in into an uninterrupted power supply (UPS). As shown in the next image, you connect the UPS to the wall outlet and the computer to the UPS. 

<img width="777" alt="image" src="https://user-images.githubusercontent.com/66931789/187051491-65473ad2-2c9d-4c39-b27a-f02ab83502c2.png">

The computer and the UPS serve separate purposes. Each has a **SINGLE RESPONSIBILITY** that doesn't infringe on the other unit. The UPS and computer are likely to be produced by two different manufacturers, bought at different times, and plugged in separately. As the image above demonstrated, you can run the computer without a UPS, and you could also conceivably use the hair dryer during blackouts by plugging it into the UPS. 

In software design, this way of INTERCEPTING one implementation with another implementation OF THE SAME INTERFACE IS KNOWN AS THE **DECORATOR** design pattern. It gives you the ability to incrementally introduce new features and CROSS-CUTTING CONCERNS without having to rewrite or change a lot of existing code. 
Another way to add new functionality to an existing code base is to refactor an existing implementation of an interface with a new implementation. When you aggregate several implementations into one, you use the COMPOSITE design pattern. 

You sometimes find yourself in situations where a plug doesn't fit into a particular socket. If you've traveled to another country, you've likely noticed that sockets differ across the world. If you bring something like the camera in the next image you will need an adapter to charge it. Appropriately, there's a design pattern with the same name. 

<img width="802" alt="image" src="https://user-images.githubusercontent.com/66931789/187051728-135ac2d1-bfda-4e4e-8ff2-a6d13c23b07b.png">

The advantage of loose coupling is the same in software design as it is in the physical socket and plug model: once the infrastructure is inplace, it can be used by anyone and adapted to changing needs and unforeseen requirements without requiring large changes to the application code base and infrastructure. This means that ideally, a new requirement should only necessitate the addition of a new class, with no changes to other already-existing classes of the system. 
This concept of being **able to extend an application without modifying existing code is called the OPEN/CLOSED PRINCIPLE.** It's impossible to get to a situation where 100% of your code will always be OPEN for extensibility and CLOSED for modification. Still, loose coupling does bring you closer to that goal. 








