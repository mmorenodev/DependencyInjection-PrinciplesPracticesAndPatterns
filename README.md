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
