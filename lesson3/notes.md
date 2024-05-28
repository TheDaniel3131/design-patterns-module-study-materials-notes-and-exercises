# Lesson 3

## Impetus ("impetus" refers to the driving force or motivation) behind the use of patterns:
- Designing reusable software is hard: Creating software that can be easily reused in different contexts is challenging. It requires careful planning and design to ensure that the software components are flexible, modular, and adaptable to various scenarios. Achieving reusability involves addressing different requirements and anticipating future changes, which can be complex.
  
- Novices are overwhelmed: Beginners in software development often find it difficult to manage the complexity of designing software. They might struggle with understanding best practices, design principles, and the nuances of creating efficient and maintainable code. The sheer volume of information and the number of decisions that need to be made can be overwhelming for those who are new to the field.
  
- Experts draw from experience: Experienced developers rely on their knowledge and past experiences to solve problems and design software. They have encountered various challenges and have learned effective solutions over time. This experience allows them to recognize patterns and apply proven techniques to new problems, making their design process more efficient and effective.
  
- Some design solutions reoccur: Certain problems and solutions tend to appear repeatedly in software development. These recurring solutions, known as patterns, address common challenges that arise in many projects. By identifying and documenting these patterns, developers can apply them to new situations, saving time and effort.

- Understanding reoccuring solutions in beneficial in several ways.
   - Efficiency: By using established patterns, developers can avoid reinventing the wheel and quickly implement solutions that are known to work.
   - Consistency: Patterns provide a consistent approach to solving problems, making the software more predictable and easier to maintain.
   - Communication: Patterns serve as a shared language among developers, facilitating better communication and collaboration within teams.
   - Quality: Patterns are often derived from best practices and have been refined over time, leading to higher-quality software.
   - Learning: For novices, understanding patterns can help them learn from the experience of experts and improve their own design skills more rapidly.

## Why Patterns (Design Patterns) and What it is?
### Why Patterns (Design Patterns)?
Efficiency: Design patterns provide standard solutions to common problems, saving time and effort by avoiding the need to reinvent the wheel. This can accelerate the development process.

Reusability: Patterns encapsulate best practices and proven techniques that can be reused across different projects and contexts, enhancing the modularity and flexibility of the code.

Consistency: Using design patterns ensures a consistent approach to solving problems, which makes the codebase more predictable and easier to maintain. This consistency is particularly valuable in large teams or long-term projects.

Communication: Patterns create a common vocabulary among developers. When a specific pattern is mentioned, it conveys a wealth of information quickly and clearly, facilitating better communication and collaboration within and between teams.

Quality Improvement: Patterns are derived from best practices and have been refined over time. By applying these patterns, developers can avoid common pitfalls and ensure a higher quality of software design.

Problem-Solving Framework: Patterns provide a structured approach to problem-solving. They guide developers in identifying the most appropriate solutions based on the context and specific requirements.

Learning Tool: For novice developers, design patterns serve as an educational resource. They offer insights into effective design principles and help beginners understand how experienced developers tackle common problems.

### What is a Design Pattern?
- **A Design Pattern is a reusable and tested solution to a reoccuring problem.**
- A Design Pattern is a general, reusable solution to a commonly occurring problem within a given context in software design. It is not a finished design that can be transformed directly into code, but rather a template or blueprint for how to solve a problem in various situations.
- Defined as description of communicating objects and classes that are customized to solve general edsign problem in particular context.
- A methodology tells you how to write down the decisions you have made, a pattern tells you which decision to make, when and how to make them, and why they are right.

- Design patterns typically include the following elements.  Design Paterns: Essentials:
  
  - Pattern Name: A descriptive name that conveys the essence of the pattern and facilitates discussion and communication.
  
  - Problem: A description of the specific problem that the pattern addresses, including the context in which it occurs and the goals that need to be achieved.
  
  - Solution: A general arrangement of objects and classes, along with their relationships, responsibilities, and collaborations, that provides a solution to the problem. The solution is often described in a way that can be adapted to different situations.
  
  - Consequences: A discussion of the results and trade-offs of applying the pattern, including potential benefits and drawbacks.

### Common Categories of Design Patterns
- Design patterns are often categorized into three main types:

  - Creational Patterns: These patterns deal with object creation mechanisms, aiming to create objects in a manner suitable for the situation. Examples include the Singleton, Factory Method, and Abstract Factory patterns.
  
  - Structural Patterns: These patterns focus on the composition of classes and objects, helping to form large structures by combining objects and classes. Examples include the Adapter, Composite, and Decorator patterns.
  
  - Behavioral Patterns: These patterns are concerned with algorithms and the assignment of responsibilities between objects. They help manage complex control flows and interactions. Examples include the Observer, Strategy, and Command patterns.

### Gang of Four (GoF)
The term "Gang of Four" (GoF) refers to the four authors of the seminal book on design patterns titled "Design Patterns: Elements of Reusable Object-Oriented Software." These authors are:

Erich Gamma
Richard Helm
Ralph Johnson
John Vlissides

#### About the Gang of Four Book
Publication Date: The book was first published in 1994 and has since become a foundational text in the field of software engineering.

- Purpose: The primary aim of the book is to provide a catalog of simple and succinct solutions to common design problems in object-oriented software development. By documenting these recurring solutions, the authors sought to standardize best practices and improve the overall quality and efficiency of software design.

##### Key Contributions
- Design Pattern Catalog: The book presents 23 design patterns, which are divided into three categories:

  - Creational Patterns: Focus on object creation mechanisms.
  - Structural Patterns: Deal with the composition of classes or objects.
  - Behavioral Patterns: Concerned with object interaction and responsibility.
  
- Pattern Structure: Each pattern in the book is described in a consistent format, including:
   -  Pattern Name: A descriptive name for the pattern.
   - Intent: The goal or purpose of the pattern.
   - Motivation: A scenario or example illustrating the problem and how the pattern solves it.
   - Applicability: Situations where the pattern is applicable.
   - Structure: A graphical representation of the pattern's classes and objects.
   - Participants: The classes and objects involved in the pattern and their roles.
   - Collaborations: How the participants interact with each other.
   - Consequences: The results, benefits, and trade-offs of using the pattern.
   - Implementation: Tips and techniques for implementing the pattern.
   - Sample Code: Example code demonstrating the pattern in practice.
   - Known Uses: Examples of the pattern in real-world systems.
   - Related Patterns: Other patterns that are related to or can be combined with the pattern.
   - Standardization of Terminology: The GoF book has standardized the terminology and concepts used in design patterns, making it easier for developers to communicate and collaborate.

#### Influence on Software Engineering: The concepts and patterns introduced by the GoF have had a profound impact on the field of software engineering. They have influenced many aspects of software development, including frameworks, libraries, and development methodologies.

##### Examples of GoF Design Patterns:
Here are a few examples of the design patterns from the GoF book:

- Singleton Pattern (Creational): Ensures a class has only one instance and provides a global point of access to it.
- Factory Method Pattern (Creational): Defines an interface for creating an object, but lets subclasses alter the type of objects that will be created.
- Adapter Pattern (Structural): Allows incompatible interfaces to work together by wrapping an existing class with a new interface.
- Observer Pattern (Behavioral): Defines a one-to-many dependency between objects so that when one object changes state, all its dependents are notified and updated automatically.
- Strategy Pattern (Behavioral): Defines a family of algorithms, encapsulates each one, and makes them interchangeable. Strategy lets the algorithm vary independently from the clients that use it.
