# What's Cotheca?
An open source effort to ease software development, together.

## Vision
Commit a better life.

## Mission
To write the most universal collection of code that anyone could use to help more ideas and dreams become a reality.

# Inspiration
A pretty awkward fact is that Software Development is a very demanding activity that limits the reach of smaller teams. So just imagine what's in for those projects or ideas driven by a single individual.

Developing an app or system that could ultimately have a positive impact in our lives requires a generous amounts of resources, from which time and effort are the most valuable of all. And that is exactly why several really great ideas, just cannot happen.

Software developers and software engineers spend a ridiculous amount of time writing and rewriting code about the most common things and concepts throughout their careers because the scope of most software focuses only in specific things of our lives without sharing common definitions or functionality of things and concepts that surround us and yet most of these are used over and over in most applications and systems that exist. Ironically, these common concepts or entities are the base of every system or application out there. Of course, every application or system has its very own definition of a "person," a "phone number," an "address," an "error," and so on. But, how different could multiple definitions for a phone number, a person's name, or a postal code, really be?

Let's image a different scenario... What if instead of re-inventing the wheel or just copying and pasting code over and over, all of these "common" concepts lived in a collection than anyone could use, just like it has already happen to other creative assets such as icons or fonts? That way it would be easier for anyone, to just focus on the parts that are unique to each application or system and that's it!

Well, that's Cotheca.

# Goals
As an open-source project, the whole objective is: "to write the most [reusable and] universal collection of code." The principal idea is to publish reusable "blocks" that any developer, engineer or aficionado can easily import into their projects for whatever purposes (personal, philanthropic, institutional or commercial). This is definitely a very conceptual and abstract objective by any realistic standard. So, let's break it down in more tangible goals, where each goal is its own project and we will see how far these get:
 - **Entity**: "A collection of common object definitions."
Provide a solid foundation to represent as many common concepts and real-world objects in code.
For example, define "Person," "Address," and "PhoneNumber" classes; and maybe, a "User" class might be implemented by inheriting from the "Person" class and adding an Address property of type "Address," a couple of phone number properties of class "PhoneNumber."
Particular **objectives for "Entity"** are:
	 - Define Data Transfer Objects
	 - Define Value Objects (implementing DTO's)
	 - Provide data validation layer for entities.
	 - Test entities and their methods with unit tests.
	 - Provide easy to read and understand documentation for adopters.
 - **Extensions**: "Extended functionality for data types."
 Provide extension methods (or polyfills) for common actions on primitive data types.
 For example, implement extension methods for the "string" data type that converts text into camelCase, PascalCase, snake_case and kebab-case by adding the methods ToCamelCase(...), ToPascalCase(...), ToSnakeCase(...), ToKebabCase(...) to the string data type.
 Particular **objectives for Extensions** project are:
	 - Implement common actions.
	 - Provide validation (where possible).
	 - Test extension methods with unit tests.
	 - Provide easy to read and understand documentation for adopters.
 - **Data Sets**: "Sets of records for commonly-used data in software."
 Provide sets of data records for commonly used data, like countries, states and cities.
 Particular objectives for Data Sets project are TBD, as this might be built on top of the "Entity" project.

The ultimate goal is to make the deliverables of these projects available in as many programming languages as possible. Once completed, deliverables will be distributed via the most commonly used package manager for each language to make it easy to integrate them into any project. Once published and available, coders could easily skip the most burden tasks for most projects.
