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
- [General Abstraction](#defining-general-abstraction)
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


### Defining Core Principles and Concepts
The current focus for this document is on how to write code for universal and reusable code libraries. When writing code, we need to remember that we are creating just building blocks at Cotheca. These blocks can and will be used for a particular purpose. However, the end product can be anything, and some fraction of it will rely on the building block you authored. That is why General Abstraction is the fundamental concept behind Cotheca, and the rest of the concepts help us to achieve such abstraction and reusability.

For readability, this section will only provide a very brief definition for each principle and concept and a few parameters or tips on what is relevant for Cotheca about that particular principle or concept. You will find code examples with a more detailed explanation for the logic used in the next section [Applying Core Principles and Concepts](#applying-core-principles-and-concepts). This way, it should be easy to skim through the concepts, but dig into the technical details only when needed.

#### Defining General Abstraction
Although *Abstraction* is a fundamental concept in Object-Oriented Programming, for this particular document, *General Abstraction* refers to simplifying complex systems or details by focusing on the most important aspects. It involves creating a clear and manageable representation of something while establishing a broader perspective on things and how they relate to each other.

To illustrate, let's imagine that our code libraries are bicycle parts. We don't know what the bicycle is for or how the bicycle is going to work. We need to assume that the end product (the bicycle) could be exclusively assembled using the parts that we provide. But more importantly, it should be possible to combine our parts with others for a more versatile and agile approach.

It's crucial to understand that at Cotheca, each program or project might exclusively develop parts related to specific functionalities of the bicycle. For instance, one program could focus exclusively on developing parts related to the drivetrain functionality of the bicycle, for which the products include cassettes, derailleurs, cranks, chain, etc. Another program or project might handle parts related solely to the traction functionality, such as wheels and rims. This analogy represents the realm of programs at Cotheca: the scope of a project, and where a particular piece might fit within a part (structure of a repository). All of this will click better as we explore more principles and concepts to define logical domain constraints and separation of concerns for our code.

Please see [Applying General Abstraction](#applying-general-abstraction) for an explained code example.


### Applying Core Principles and Concepts
This section demonstrates how Core Principles and Concepts are applied to Cotheca's software architecture, development practices and coding style by providing a code example.


#### Applying General Abstraction
This is a weird concept to begin this section with, but it is the most important concept for the whole Cotheca project. General Abstraction is not a checklist you can follow to write your code or a formula you can just apply to revise your code. Instead, it is the result of applying all of the other "Core Principles and Concepts".

This "Applying General Abstraction" sub-section of "Applying Core Principles and Concepts" will, however, help you grasp what Cotheca is trying to do, in a more tangible way.


##### General Abstraction Relevance
What's relevant about [General Abstraction](#defining-general-abstraction) at Cotheca?
- It helps to describe business logic through the code itself.
- It helps break down processes into clear steps, tasks, or smaller processes.
- It establishes a clear separation of concerns as a result.
- It embraces and re-inforces code interoperability.
- It helps to identify concepts and objects that could be re-utilized somewhere else.
- It helps to define a higher perspective of things that could lead to re-utilizing our source code on different parts of a project, or even for different applications.
- Identify other Cotheca products that could be used in our projects and provide a more standard approach to a specific process or application.
- It improves development operations and project management when leveraging DevOps features in GitHub, programming language features and programming concepts.
  - For example:
    - Issues in GitHub can be created when new entities, methods or classes are identified.
	- General Abstraction can be applied by defining interfaces, treating interfaces as pseudo-code or the abstract contract of what a particular class or process should support and acomplish.
	- Interface definitions could be used when creating issues (more likely feature requests) to delegate development activities.
	- Interfaces can be used as a blue print for other projects or products even when the interfaces have not be implemented yet. Even issues can reference issues to automatically keep track of the actual implementation of the interfaces accelerating complex projects.
	- Intellisense and other built-in IDE features can accelerate developer conversion and smooth learning process

##### General Abstraction Code Example
Let's suppose that we are going to build a generic tool to help architects to calculate the materials needed for quoting small projects. Let's over-simplify this: let's suppose our program calculates the area of a circle with a radius of 5 meters and the area of a rectangle measuring 4 meters by 6 meters.

###### General Abstraction Example Initial Code
Initial code for the scenario:
```csharp
using System;

class Program
{
    static void Main()
    {
	    // Define values
	    var CircleRadius = 5; // meters
	    var RectangleWidth = 4; // meters
	    var RectangleHeight = 6; // meters

		// Calculate Areas (in square meters)
		var CircleArea = Math.PI * CircleRadius * CircleRadius; // 78.53...
		var RectangleArea = RectangleWidth * RectangleHeight; // 24

        // Display the data
        Console.WriteLine
        (
	        $"Circle Area: {CircleArea}, " +
	        $"Width: {CircleRadius * 2}, " +
	        $"Height: {CircleRadius * 2}"
		);
		// Output:
		// Circle Area: 78.54, Width: 10, Height: 10
        
        Console.WriteLine
        (
	        $"Rectangle Area: {RectangleArea}, " +
	        $"Width: {RectangleWidth}, " +
	        $"Height: {RectangleHeight}"
        );
        // Output:
        // Rectangle Area: 24, Width: 4, Height: 6
    }
}
```

Even for this over-simplified scenario, we can identify the following in our code:
- Our code usage is very limited
- The program is about geometric shapes, specifically about the "abstract" concept of a 'shape'
- If we wanted to calculate another shape area, we would need to declare more variables to store the information for the shapes in 'Main'
- The code for displaying the information is very similar
- We have repetitive logic

###### General Abstraction Example Code
Resulting code after applying relevant General Abstraction:
```csharp
using System;
// Initially we notice that we can extract the "Shape" concept from the intial code

// We notice some common properties and methods right away,
// so we outline an interface to define what a Shape is and what it should do:
interface IShape {
	// Notice we are defining ONLY the getter for the Name property at the interface level,
	// because we only expect Shape to let other access it's name, but not set it or overwritte it
	public string Name { get; }
	public double Width { get; set; }
	public double Height { get; set; }
	
	public double CalculateArea();
}

// Let's define an abstract class as a semi-concrete implementation for the IShape interface.
// We implement an abstract class because it allows us to expand on the blueprint the interface provides
// by defining class behavior and logic shared across all concrete implementation for the class,
// and even give us room for letting subclasses determine some behavior.
abstract class Shape : IShape
{
	// Define properties found in all shapes
    public string Name
    { 
	    get;
		// Notice that even we are implementing the IShape interface,
		// we are also defining a setter (which is not part of the IShape interface)
		// because we want to allow subclasses to set the name,
		// but we do not want external code to modify the name of the shape.
	    protected set;
    }
    public double Width { get; set; }
    public double Height { get; set; }

    // Abstract method for calculating area
    public abstract double CalculateArea();

    // Override ToString to generate the message
    public override string ToString()
    {
        return $"{Name} Area: {CalculateArea()}, Width: {Width}, Height: {Height}";
    }
}

// Concrete class Circle inheriting from Shape
class Circle : Shape
{
	// Radius is only found in circles
	public double Radius { get; set; }

    // Define a constructor
    public Circle()
    {
	    // Programmatically assign the shape name:
        Name = nameof(Circle); // "Circle"
    }

    // Implementing the abstract method to calculate the area of a circle
    public override double CalculateArea()
        => Math.PI * Radius * Radius;
}

// Concrete class Rectangle inheriting from Shape
class Rectangle : Shape
{
    public Rectangle()
    {
	    // Programmatically assign the shape name:
        Name = nameof(Rectangle); // "Rectangle"
    }

    // Implementing the abstract method to calculate the area of a rectangle
    public override double CalculateArea()
        => Width * Height;
}


public class Program
{
	public static void Main()
	{
		// Create instances of Circle and Rectangle
        var circle = new Circle
        {
	        Radius = 5,
			Width = 10, // Radius * 2
			Height = 10 // Radius * 2
        };

        var rectangle = new Rectangle
        {
            Width = 4,
            Height = 6
        };

        // Use the ToString() method to generate and display the messages
        Console.WriteLine(circle);
        Console.WriteLine(rectangle);
	}
}
```

###### General Abstraction Code Example Takeaways
- Extracted both an interface (`IShape`) and an abstract class (`Shape`) to represent a higher recurring concept in our lives that is potentially used somewhere else, given that it's not exclusive to our logic and can be shared without revealing sensitive business logic about our application.
- Extracted two classes that represent common concepts or objects in our lives, potentially used elsewhere given that they are not exclusive to our logic and can be shared without revealing sensitive business logic about our application.
- Although code might be more extensive because new classes were extracted, the actual exclusive logic of the program was reduced to only two meaningful tasks (Define values, Display data); this is down from the initial four meaningful tasks (Define values, Calculate areas, Get and format data, Display the data).
- By centralizing logic into intuitive places in relation to the concepts used in the code, the probability of introducing errors or bugs to the code was reduced significantly because there's no repetitive logic.
- Potentially, the shared shape classes could allow the application to integrate with other systems, libraries, or programs, and only unique logic needs to be written to accomplish their unique objectives for those applications, libraries, or systems.

###### General Abstraction Code Example Issues To Watch
- Implicit operations were introduced (`CalculateArea()` method is called in the `ToString()` method, which is implicitly called by the `WriteLine()` method):
    - This logic or this style of code might be more challenging to troubleshoot or understand.
    - In this example, implicit logic was used for illustration purposes only.
    - In a real-world Cotheca product, prefer explicit logic over implicit logic when the use of implicit is not obvious:
        - You have a few options (in order of preference) when leveraging implicit logic in a Cotheca product:
            - Add a test with the expected behavior so if anything changes at any point, it is easier or even automatic to detect when running tests.
            - Use code to make it obvious that implicit logic is intended, sort of the principle behind using `string.Empty` over `""` in C#.
            - Add a comment. It's the worst case scenario, but still acceptable.
- Huge assumptions were made for illustration purposes.
    - Unique logic from the application was implemented in the `ToString` method of the abstract class (intended to be shared).
    - In a real-world Cotheca product, do not implement exclusive or business logic into the shared libraries. Remember that Cotheca libraries are intended to be universal.
	- All classes were implemented in the same file for simplicity. In a real-world case, each interface and class would have been implemented in a seperate file each, in their respective repositories, projects, and namespaces and referenced accross.
- Other "higher" concepts could have been implemented:
    - To keep the code example simple, other relevant real-life objects or concepts were intentionally omitted.
    - In a real-world Cotheca product, General Abstraction must be applied as much as possible (to a realistic, feasible, and functional extent):
        - If the new classes aren't part of the scope of the project, please request the features in their respective repository's issues. Otherwise, submit a new issue to the Development board. If working on a PBI, update the issue you are working on and tag the new issue as a blocker for the current PBI.
    - Just to illustrate, the following higher concepts or objects were omitted:
        - Measuring Unit: An abstract class representing the abstract concept of "a measure."
        - Linear Unit: An abstract class, inheriting from the "Measuring Unit" class, representing the abstract concept of a linear unit.
        - Area Unit: An abstract class, inheriting from the "Measuring Unit" class, representing the amount of surface a two-dimensional shape can cover.
        - Meter: A concrete class, inheriting from the "Linear Unit" class, representing a metric meter.
        - Square Meter: A concrete class, inheriting from the "Area Unit" class, representing a metric square meter.

Yeah, this could get a bit too deep into the rabbit hole and existential. That's what I meant about being a weird concept, because it's such an abstract concept on its own and feels too niche. As a code author, you might question what's convenient about expanding code into an over-engineered version of it, when at a functional-level it changes nothing. Right?

If you have authored code before, you will be familiar with the feeling of rewriting some code over and over again, probably to the point that you have copied and pasted code from one project to another, then made some improvements on some copies and then expected to have the improved version in another project that does not have it. So, either you keep copying and pasting versions across projects or simply lose work by losing track of which project you made the desired improvements to.

Or, you might even be familiar with the feeling of having a project idea, but the foundation of the project takes the most effort or time to code, and it's the most generic part of the project, keeping it in an "in progress" state or in a to-do list because time is becoming the most valuable resource in our current era. Such a scarce one.

The overall objective of general abstraction is to bring ease, clarity, and functionality at higher levels. It could be really worth it at so many different levels.
