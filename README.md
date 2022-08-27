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

What happens when the hair dryer stops working?



