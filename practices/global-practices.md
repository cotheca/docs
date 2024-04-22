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
- [Object-Oriented Programming (OOP)](#defining-object-oriented-programming)
  - [Inheritance](#defining-inheritance)
  - [Encapsulation](#defining-encapsulation)
  - [Abstraction](#defining-abstraction)
  - [Polymorphism](#defining-polymorphism)
  - [Composition](#defining-composition)
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

#### Defining Object-Oriented Programming
Object-Oriented Programming (OOP) is a programming paradigm based on the concept of "objects," which can contain data describing the object's attributes or properties, as well as actions, in the form of methods. OOP allows developers to organize software as a collection of discrete objects that incorporate both data structures and behavior.

At Cotheca, OOP helps in crafting code that is modular, easy to manage, and reusable. Objects created as part of a product can often be reused in other projects, whether it's for another Cotheca product or an external product or project. This modularity supports our goal of creating software libraries that can be easily shared across different projects and environments, enhancing both universality and reusability. OOP's emphasis on encapsulation, polymorphism, and inheritance aligns with our architectural philosophies by promoting clean and maintainable code structures that simplify both development and future enhancements. We will be covering the specifics of these OOP Principles and Concepts in terms of defining them, explaining what are the relevance of them in the Cotheca Project and actual code examples the following sub-sections of the document:

- Inheritance
	- [Defining Inheritance](#defining-inheritance)
	- [Applying Inheritance](#applying-inheritance)
- Encapsulation
	- [Defining Encapsulation](#defining-encapsulation)
	- [Applying Encapsulation](#applying-encapsulation)
- Abstraction
	- [Defining Abstraction](#defining-abstraction)
	- [Applying Abstraction](#applying-abstraction)
- Polymorphism
	- [Defining Polymorphism](#defining-polymorphism)
	- [Applying Polymorphism](#applying-polymorphism)
- Composition
	- [Defining Composition](#defining-composition)
	- [Applying Composition](#applying-composition)

The programming paradigm approach used at Cotheca is a hybrid one, combining OOP and Functional Programming. Don't worry we'll cover Functional Programming in more detail in future sections, so let's focus on OOP for now. Cotheca projects leverage both paradigms depending on the purpose of the code. OOP is great for structuring data in "value objects", and especially data transfer objects (DTOs) while Functional Programming is amazing for processing data objects and computing data. For example, OOP allows us to categorize objects that share characteristics and use other objects to describe properties or characteristics of them, as well as share some common logic. By definition, data transfer objects should not contain any business logic; however, we might use non-mutable data-related common logic as part of the object definitions and super classes definitions depending on how general or specialized our code is. This a somewhat of a middle ground between value objects and DTO's. Some logic that could be part of objects could be methods for data presentation, data transformation, data validation, data or object equality. Additionally, in most scenarios, shared logic can be added to classes via extension methods (or similar paradigms) as a middle ground of implementing object-oriented behavior in a more portable and interoperable approach.

You can find explained code examples on how to apply OOP in these sections:
- [Applying Inheritance](#applying-inheritance)
- [Applying Encapsulation](#applying-encapsulation)
- [Applying Abstraction](#applying-abstraction)
- [Applying Polymorphism](#applying-polymorphism)
- [Applying Composition](#applying-composition)

#### Defining Inheritance
Inheritance in Object-Oriented Programming (OOP) is a mechanism that allows us to define a new class based on an existing class. The new class, known as a child class, inherits attributes and behaviors (methods) from the existing class, which is referred to as the parent class. This fundamental OOP concept enables a hierarchy of classes that promotes code reusability and organization.

At Cotheca, embracing inheritance means we can create a structured and scalable codebase. For example, if we have a general class called `Vehicle`, we can inherit this class to create specific types of vehicles like `Car`, `Bike`, or `Truck`. Each of these subclasses can then add its specific attributes and methods while inheriting common characteristics from the `Vehicle` class. This helps prevents redundancy and ensures that each component or module we develop can interact seamlessly with others, maintaining a consistent architecture across our projects.

Inheritance promotes an intuitive way to think about our code libraries: as a family tree where each new class represents a more specific, or specialized version of its parent. Allowing us to produce universal, reusable, and modular software components that support a wide range of applications while simplifying maintenance and upgrades.

Please see [Applying Inheritance](#applying-inheritance) for an explained code example.


#### Defining Encapsulation

#### Defining Abstraction

#### Defining Polymorphism

#### Defining Composition

#### Defining Functional Programming

#### Defining First-Class Functions

#### Defining Immutability

#### Defining Pure Functions

#### Defining High-Order Functions

#### Defining Modularity

#### Defining Data Normalization

#### Defining Do Not Repeat Yourself

#### Defining Clean Architecture

#### Defining Domain-Driven Design

#### Defining Code Interoperability


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


#### Applying Inheritance
This section highlights how the core concept of Inheritance is fundamental in building scalable and maintainable software within the Cotheca Project.

##### Inheritance Relevance
What is relevant about [Inheritance](#defining-inheritance) at Cotheca?
- Allows us to extract higher concepts and expand value objects from them
- Establishes a natural hierarchy in data objects
- Reduces single point of failure in our models, by sharing logic from a single source of truth or a shared centralized location
- Enhances code reusability and portability
##### Inheritance Code Example
Let's imagine we are developing a mileage logging app for vehicles. At this stage of the application we are registering the mileage for a few vehicles.

###### Inheritance Example Initial Code
So, we have the following code so far:

```csharp
using System;

// Define the classes that will store the data
class Car {
	public string Make { get; init; }
	public string Model { get; init; }
	public int Year { get; init; }
	public int Odometer { get; init; } // In Miles
	
	public void DisplayMileage()
		=> Console.WriteLine($"Current odometer (in miles): {Odometer}");
		
	public string GetDisplayModel()
		=> $"{Year} {Make} {Model}";
}

class Truck {
	public string Make { get; init; }
	public string Model { get; init; }
	public int Year { get; init; }
	public int Odometer { get; init; } // In Miles
	
	public void DisplayMileage()
		=> Console.WriteLine($"{Odometer} miles");
		
	public string GetDisplayModel()
		=> $"{Year} {Make} {Model}";
}

class Bicycle {
	public string Make { get; init; }
	public string Model { get; init; }
		
	public string GetDisplayModel()
		=> $"{Make} {Model}";
}

class ElectricBicycle {
	public string Make { get; init; }
	public string Model { get; init; }
	public int Odometer { get; init; } // In Miles
	
	public void DisplayMileage()
		=> Console.WriteLine($"Traveled miles: {Odometer}");
		
	public string GetDisplayModel()
		=> $"{Make} {Model}";
}

public class Program
{
	public static void Main()
	{
		// Define the values
		var myCar = new Car()
		{
			Make = "Toyota",
			Model = "Corolla",
			Year = 2022,
			Odometer = 38450
		};
		
		var myTruck = new Truck()
		{
			Make = "Tesla",
			Model = "CyberTruck",
			Year = 2024,
			Odometer = 441
		};
		
		var myBike = new Bicycle()
		{
			Make = "Trek",
			Model = "Marlin 4"
		};
		
		var myEbike = new ElectricBicycle()
		{
			Make = "Co-Op Cycles",
			Model = "DRT e3.1",
			Odometer = 499
		};
		
		
		// Display the data
		myCar.DisplayMileage();
		// Output:
		// Current odometer (in miles): 38450
		
		myTruck.DisplayMileage();
		// Output:
		// 441 miles
		
		myEbike.DisplayMileage();
		// Output:
		// Traveled miles: 499
	}
}

```

Even after taking into consideration the simplicity of the program, from the example, we can identify the following (from an object-oriented perspective):
- All of these objects share a couple of properties and a method
- Some of these vehicles do not have an odometer
- Similar methods generate different outputs or results
- Classes are more than just value objects, they have some methods that are considered "business logic" as this are specific to the application.
- There some conceptual ambiguity for class `ElectricBicycle` as this class share properties with `Truck`, `Car` and `Bicycle`

###### Inheritance Example Code
Let's apply Inheritance to see how can we make things better in terms of re-usability and maintenance:

```csharp
using System;

// Define the classes that will store the data

// All of this are types of vehicles, so let's move all common properties into a new Vehicle class:

// But first, let's define a contract of which properties and methods should make up a Vehicle by definig an interface
public interface IVehicle
{
	public string Make { get; }
	public string Model { get; }
	
	public string GetDisplayModel();
}

public class Vehicle: IVehicle
{
	// All of the classes share this properties
	public string Make { get; init; }
	public string Model { get; init; }
	
	// Let's add this common method as it's still conceptually universal
	public string GetDisplayModel()
		=> $"{Make} {Model}";
}

// There's some properties that are shared by some vehicles but not all of them,
// so we can use subclass of Vehicle for those

// Let's create a new interface for Vehicles with an odometer. Overall speaking this is a business logic interface
public interface IReadableOdometer
{
	int Odometer { get; }
}

// Just for illustration purposes we will be adding a type of motor enum
public enum MotorType
{
	Unknown,
	Gasoline,
	Electric
}

// This is a universal concept, so we will be 
public class MotorVehicle : Vehicle
{
	public MotorType MotorType { get; init; } = MotorType.Unknown;
}

// Also, theres some common attributes between Car and Truck, but not for the bicycles,
// so let's define a more specific class for 4-wheeled motor vehicles
public class Automobile : MotorVehicle
{
	public int Year  { get; init; }
	
	// Automobile Models are displayed in a common format,
	// so let's add the year to the output of the Vehicle class
	new public string GetDisplayModel()
		=> $"{Year} { base.GetDisplayModel() }";
}

// So far we have defined several universal classes, but we are still missing the odometer property.

// Let's use an extension method for business logic
internal static class OdometerExtensions
{
	public static void DisplayMileage(this IReadableOdometer vehicleWithOdometer)
		=> Console.WriteLine($"Current odometer (in miles): {vehicleWithOdometer.Odometer}");
}

// Our application objective is to log odometer readings. That's business logic too.
internal class MyAppAutomobile : Automobile, IReadableOdometer
{
	public MyAppAutomobile()
	{
		MotorType = MotorType.Gasoline;
	}

	public int Odometer { get; init; } = 0; // In miles
}

// To centralize default behavior for electric cars and trucks we create a new class 
internal class ElectricAutomobile: MyAppAutomobile
{
	public ElectricAutomobile()
	{
		MotorType = MotorType.Electric;
	}
}

internal class Car : MyAppAutomobile {}
// We keep our original Truck class for backward compatibility,
// but we integrate it to our new class design
internal class Truck : MyAppAutomobile {}
internal class ElectricTruck : ElectricAutomobile {}
internal class Bicycle : Vehicle {}

// We want to still support e-bikes, but we want to keep our code portable
// and universable where applicable, so let's create a new class combining
// universal value objects and our own business logic.
internal class ElectricBicycle : MotorVehicle, IReadableOdometer
{
	public ElectricBicycle()
	{
		MotorType = MotorType.Electric;
	}
	
	public int Odometer { get; init; } = 0; // In miles
}

public class Program
{
	public static void Main()
	{
		// Define the values
		// This time we will store the values into a single variable,
		// a collection of Vehicles,
		// instead of storing the data into individual hard-coded variables
		var myVehicles = new Vehicle[]
		{
			// Of course we can store an instance of Car!
			// Car is a subclass of Vehicle,
			// because Car is a subclass of Automobile,
			// Automobile is a subclass of MotorVehicle,
			// and MotorVehicle is a subclass of Vehicle
			new Car()
			{
				Make = "Toyota",
				Model = "Corolla",
				Year = 2022,
				Odometer = 38450
			},
			
			// Of course we can store an instance of Truck!
			// Truck is a subclass of Vehicle,
			// because Truck is a subclass of Automobile,
			// Automobile is a subclass of MotorVehicle,
			// and MotorVehicle is a subclass of Vehicle
			new ElectricTruck()
			{
				Make = "Tesla",
				Model = "CyberTruck",
				Year = 2024,
				Odometer = 441
			},
			
			// Of course we can store an instance of Bicycle!
			// Bicycle is a subclass of Vehicle
			new Bicycle()
			{
				Make = "Trek",
				Model = "Marlin 4"
			},
			
			// Of course we can store an instance of ElectricBicycle!
			// ElectricBicycle is a subclass of Vehicle,
			// because a ElectricBicycle is a subclass of MotorVehicle,
			// and MotorVehicle is a subclass of Vehicle
			new ElectricBicycle()
			{
				Make = "Co-Op Cycles",
				Model = "DRT e3.1",
				Odometer = 499
			}
		};
		
		
		// Display the data
		
		// We can make our program more dynamic
		foreach(var vehicle in myVehicles) {	
			if(vehicle is IReadableOdometer vehicleWithOdometer)
			{
				// What output would you expect for this disabled code block?
				var displayExtraInfo = false;
				if( displayExtraInfo && vehicle is MotorVehicle motorVehicle )
				{
					var model = (motorVehicle is Automobile automobile)
						? automobile.GetDisplayModel()
						: motorVehicle.GetDisplayModel();
					
					switch(motorVehicle.MotorType)
					{
						case MotorType.Electric:
							Console.WriteLine($"{ model } is an electric vehicle:");
							break;
						case MotorType.Gasoline:
							Console.WriteLine($"{ model } is a gasoline vehicle:");
							break;
					}
				}
				
				
				vehicleWithOdometer.DisplayMileage();
			}
		}
		// Output:
		// Current odometer (in miles): 38450
		// Current odometer (in miles): 441
		// Current odometer (in miles): 499
	}
}

```

###### Inheritance Code Example Takeaways
- Inheritance is highly effective only when the features and characteristics of a system or applications are accurately deconstructed and accurately placed across the software architecture domains. For Cotheca products, this means using inheritance merely for value objects that share common characteristics and features, and using inheritance side-by-side with composition.
    - Trying to enforce either inheritance or composition over the other tends to lead a lot into hard to understand and unsustainable code. This will result in a huge negative business impact in the medium or long run, causing a lot of waste of resources and outdated business processes (even when the code has outstanding technical or economic performance during run-time) for organizations.
    - There's no substitution for either. If a codebase isn't constantly updated or upgraded, because it takes a significant amount of time and involves considerable risk, then the approach taken by the authors regarding inheritance or composition is not optimal. The goal is to have agnostic agile code, not to root for inheritance or composition merely on trends or popularity of opinion. Obviously, the time and risk to maintain and upgrade should be proportional to the codebase, but it becomes really obvious that the taken approach to either inheritance or composition is not optimal when these tasks are highly avoided, or when adding a completely new feature requires a disproportionate amount of refactoring.
- Different higher level concepts were identified from the initial classes such as `Vehicle`, `MotorVehicle`, and `Automobile` by identifying common characteristics and how they relate to real-life concepts that can potentially be used elsewhere.
- Implementing inheritance didn't modify the overall program functionality, but rather added support for adding more values to the `Vehicle[]` array, added a variety of classes of vehicles that the application can handle, dynamically display the odometer reading only for those vehicles with an odometer. The only functionality that was changed was how the odometer readings are displayed, keeping the format constant across all usages, preventing the introduction of bugs whenever a new class supporting the DisplayMileage() feature defined its own way to implement this feature.
- Although it might feel like an over-engineered solution for this particular program, applying inheritance broke down classes into more re-usable and universal classes that aren't exclusive to this program.
- Inheritance adds interoperability at different levels whether each subclass data is for different purposes thanks to the inherited properties and methods that are passed from base classes to subclasses. We even have a few examples for multiple inheritance objects and how using inheritance we can model new classes that fit our business logic and still uses portable universal value objects in a realistic and sustainable way (like `MyAppAutomobile`,  `ElectricBicycle`, `ElectricAutomobile`, and `ElectricTruck`).
- The `GetDisplayModel()` method was kept a member of the base class `Vehicle` because it only transforms data for presentation purposes only and the output is not specific to a particular program, but could be considered a universal property across vehicles.
- The `DisplayMileage(...)` method was kept out of the `MotorVehicle` class because the behavior is specific to this particular program while still providing an object-oriented syntax for its usage.
- The `ElectricBicycle` class was intentionally used in the example because it would have been more intuitive to have extracted the following classes: `Bicycle:Vehicle`, `ElectricBicycle:Bicycle`; however, from a functional point of view of classes (relative to the application), `Bicycle` and `ElectricBicycle` do not share many things in common. When working on Cotheca libraries, decide hierarchy of classes by analyzing the resulting classes and see what's common in each and how it could be used in third-party applications.
- In a real-world scenario, we would have spread all of our classes into different domain levels (due to separation of concerns) [Notice the usage of different access levels for classes to reflect this, `public` access was assigned to code expected to be shared outside of the project and the `internal` access level was assigned to code expected to be used within the project]:
    - Cotheca Libraries (most universal)
        - `IVehicle` interface
        - `Vehicle` class
        - `MotorType` enum
        - `MotorVehicle` class
        - `Automobile` class
    - Organization Libraries (potentially re-usable within the organization developing the Mileage Logging application, but could have been specific to the application too)
        - `IReadableOdometer` interface
        - `MyAppAutomobile` class
        In a real-world scenario, the class name could have remained the same, `Automobile`, but namespaces could have been used to distinguish the organization/app implementation from the Cotheca implementation.
        - `ElectricAutomobile` class
        - `Car` class
        - `Truck` class
        - `Bicycle` class
        - `ElectricBicycle` class
        - `ElectricAutomobile` class
        - `OdometerExtensions` class
    - Mileage Logging application (most specific)
        - `Program`

###### Inheritance Code Example Issues To Watch
- Some assumptions were made and code does not reflect an actual Cotheca Library, but rather exemplifies how new Cotheca classes could be extracted from application code.
- Please consult the goals of specific Cotheca libraries and the functionality that is aiming to provide to design classes and determining concrete implementations and class hierarchy.
- Other higher concepts were omitted from the example that could have been implemented:
    - `MeasuringUnit`: An abstract class representing the abstract concept of "a measure"
        - `LinearUnit`: An abstract class, inheriting from `MeasuringUnit`, representing the abstract concept of a linear unit
            - `Mile`: A concrete class, inheriting from `LinearUnit`, representing an imperial mile.
- Only use inheritance for value object properties, meaning that inheritance should only provide relevant data model properties, for more specific logic implement multiple inheritance strategies that make sense in the long term for your application or organization.
- Inheritance can be really useful, but as you can see from the example it can get very confusing, hide properties, and code authors unfamiliar with the class design could introduce bugs due to being unfamiliar with the code base. Use tests, language features, and in-code documentation to establish an understandable use of inheritance that is sustainable.
- Class and interface naming can introduce bugs by getting ambiguous or unclear for custom implementations or subclasses. Use namespace strategies to help differentiate, use your project documentation to let contributors know what classes to use. Use documentation, tests, or validation rules to detect misused classes. For example, see documentation (and IDE features like IntelliSense) to inform your team that your application should use `MyOrg.Models.Vehicles.Automobile` instead of `Cotheca.ExampleLib.Vehicles.V2.Automobile` (example namespace, not a real library).

#### Applying Encapsulation
##### Encapsulation Relevance
##### Encapsulation Code Example
###### Encapsulation Example Initial Code
###### Encapsulation Example Code
###### Encapsulation Code Example Takeaways
###### Encapsulation Code Example Issues To Watch


#### Applying Abstraction
##### Abstraction Relevance
##### Abstraction Code Example
###### Abstraction Example Initial Code
###### Abstraction Example Code
###### Abstraction Code Example Takeaways
###### Abstraction Code Example Issues To Watch


#### Applying Polymorphism
##### Polymorphism Relevance
##### Polymorphism Code Example
###### Polymorphism Example Initial Code
###### Polymorphism Example Code
###### Polymorphism Code Example Takeaways
###### Polymorphism Code Example Issues To Watch


#### Applying Composition
##### Composition Relevance
##### Composition Code Example
###### Composition Example Initial Code
###### Composition Example Code
###### Composition Code Example Takeaways
###### Composition Code Example Issues To Watch
