# Global Practices
The main objective for the Cotheca project - as a whole - is to help streamline software development regardless of the environment, the programming language or even what the end-product is about by providing a global solution for common needs on most software products.

In order to achieve this ambitious objective, we need to pursue and apply several principles from software engineering and data modeling. This *Global Practices* document describes the principles used, how are they used and in which development stage they are used.

## The Big Picture for Practices
This Global Practices document establishes a written context and guidelines upon which Cotheca Contributors build universal, sharable and interchangeable software libraries for all. By following, revising or suggesting updates to these practices:
 - Software authors can understand what's the aggregated value of using Cotheca libraries in their products.
 - Cotheca Contributors can have a written reference on how to build these libraries and solutions together in an organized and efficient way, so their efforts are successfully apply to our supply chain.
 - Cotheca could help channel an important percentage of individual coding efforts from adopters from their independent endeavors into a common public code base.

## Organizational Definitions
As you will learn ahead, we adapt some philosophies and practices from Domain-Driven Design(DDD), and one of the most important principles from DDD is the use of a common language among all the people involved in something. This is also true in multiple Project Management practices, as well.

For consistency across the board, let's define some relevant terms:

### Cotheca Project
Is the formal term that encloses everything Cotheca. Actually, it could be think as a formal synonym for Cotheca. It gets a little tricky, because Cotheca is not a formal organization per se, at the time of this writing, but it does need to have a foundational organizational basis in order to be a collaborative effort.

The Cotheca Project does not currently have an organizational structure at the time. Cotheca is not an institution or physical place either. The terms *Cotheca Project* and *Cotheca* (by itself) refers to the abstract effort of pursuing the goal of delivering a "Universal code library to help accelerate and improve software development projects of individuals and organizations," hopefully as group effort.

### Repository
Generally speaking, a repository is a central location where code is stored and usually refers to a Git repository. But, in a more organizational context, it mostly refers to a GitHub repository authored and/or managed by Cotheca and its contributors. 

### Project
Oh the spicy one! The term *project* when not used in the term *Cotheca Project*, it  refers to a project being worked at Cotheca. That is, the particular effort to complete or contribute to a particular "product" with pre-determined goals or objectives.

### Product
This might get a little confusing, due to the common usage of the word "product" referring to an item or substance created or refined for the purpose of being sold. It's important to note that Cotheca does not commercialize products.

In our context, the term *product* refers to the result from our coding efforts to fulfill a singular set of pre-determined goals or objectives. Basically, the result of a *project*.

It can be used interchangeably with the terms *project* and *repository* in the Cotheca Docs, given that a particular repository is the media on which the works of a particular project is stored and managed. However, the term *Product* might be used to highlight that it is being used to refer to the final result being published and distributed, while the term *project* might refer to the development cycle efforts of a specific repository.

### Program
You will see the term *program* used every now and then, but when used in a project or organizational context, like in "... a program at Cotheca ...," it refers to a collection of projects that are related in some context and are being managed as such.


## Core Principles and Concepts
Cotheca is derived from these principles and concepts in computer science:
- Object-Oriented Programming (OOP)
  - Inheritance
  - Encapsulation
  - Abstraction
  - Polymorphism
  - Composition
- Functional Programming (FP)
  - First-class Functions
  - Immutability
  - Pure functions
  - High-order functions
- Modularity
- Data Normalization
- Do Not Repeat Yourself (DRY)
- Clean Architecture
- Domain-Driven Design (DDD)
- Code Interoperability

These Principles and Concepts can be related to each other or not at all, meaning that the way that we work with these is not a sequential process and we might use the same principle at different stages of development.

Again, the main goal of this document is to go over the logic applied in architectural decisions and how to break down entities into fundamental components, but more specifically how to apply the above principles into everyday tasks and especially establish a written reference upon which code should be written and reviewed.

Remember that this document is not set in stone. The idea is to promote a collaborative space for anyone to propose changes or improvements to achieve the overall goal of Cotheca of universality, reusability, and modularity for code.

Because of the extensive nature of this document, this "Core Principles and Concepts" section is just a brief overview of the principles and concepts that serve as a foundation for the architectural and coding practices. In the following sub-sections, you will find a definition for each of the principles and concepts mentioned above and how they are applied during the design and development stages of the Cotheca products with examples on how to apply them.


