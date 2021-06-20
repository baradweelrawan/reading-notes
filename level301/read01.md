# this is read01 from 301
# Component-Based Architecture:
![img](https://miro.medium.com/max/3408/1*Xml-O5qIRk5PGbdv9hNwxw.png)
Component-based architecture focuses on the decomposition of the design into individual functional or logical components that represent well-defined communication interfaces containing methods, events, and properties. It provides a higher level of abstraction and divides the problem into sub-problems, each associated with component partitions.
A component encapsulates functionality and behaviors of a software element into a reusable and self-deployable binary unit. There are many standard component frameworks such as COM/DCOM, 
JavaBean, EJB, CORBA, .NET, web services, and grid services.Component-oriented software design has many advantages over the traditional 
object-oriented approaches such as −
1. Reduced time in market and the development cost by reusing existing components.
2. Increased reliability with the reuse of the existing components.

# What is a Component?
A component is a modular, portable, replaceable, and reusable set of well-defined functionality that encapsulates its implementation and exporting it as a higher-level interface.A component is a software object, intended to interact with other components, encapsulating certain functionality or a set of functionalities. It has an obviously defined interface and conforms to a recommended behavior common to all components within an architecture.A software component can be defined as a unit of composition with a contractually specified interface and explicit context dependencies only. That is, a software component can be deployed independently and is subject to composition by third parties.

# A component can have three different views − object-oriented view, conventional view, and process-related view:
   1. Object-oriented view:A component is viewed as a set of one or more cooperating classes. Each problem domain class analysis and infrastructure class design are explained to identify all attributes and operations that apply to its implementation.

   2. Conventional view:It is viewed as a functional element or a module of a program that integrates the processing logic, the internal data structures that are required to implement the processing logic and an interface that enables the component to be invoked and data to be passed to it.

   3. Process-related view:instead of creating each component from scratch, the system is building from existing components maintained in a library. As the software architecture is formulated, components are selected from the library and used to populate the architecture.

# Characteristics of Components:
1. Reusability 
2. Replaceable
3. Not context specific
4. Extensible 
5. Encapsulated
6. Independent 

# Principles of Component−Based Design:
A component-level design can be represented by using some intermediary representation such as graphical, tabular, or text-based that can be translated into source code. The design of data structures, interfaces, and algorithms should conform to well-established guidelines to help us avoid the introduction of errors.
   * The software system is decomposed into reusable, cohesive, and encapsulated component units.
   * Each component has its own interface that specifies required ports and provided ports; each component hides its detailed implementation.
   * A component should be extended without the need to make internal code or design modifications to the existing parts of the component.
   * Depend on abstractions component do not depend on other concrete components, which increase difficulty in expendability.
   * Connectors connected components, specifying and ruling the interaction among components. The interaction type is specified by the interfaces of the components.

# Component-Level Design Guidelines:
Creates a naming conventions for components that are specified as part of the architectural model and then refines or elaborates as part of the component-level model:
     1. Attains architectural component names from the problem domain and ensures that they have meaning to all stakeholders who view the architectural model.
     2. Extracts the business process entities that can exist independently without any associated dependency on other entities.
     3. Recognizes and discover these independent entities as new components.
     4. Uses infrastructure component names that reflect their implementation-specific meaning.
     5. Models any dependencies from left to right and inheritance from top base class to bottom derived classes.
     6. Model any component dependencies as interfaces rather than representing them as a direct component-to-component dependency.

# Conducting Component-Level Design:
  1. Recognizes all design classes that correspond to the infrastructure domain.
  2. Describes all design classes that are not acquired as reusable components, and specifies message details.
  3. Identifies appropriate interfaces for each component and elaborates attributes and defines data types and data structures required to implement them.
  4. Describes processing flow within each operation in detail by means of pseudo code or UML activity diagrams.
  5. Describes persistent data sources databases and files and identifies the classes required to manage them.
  6. Develop and elaborates behavioral representations for a class or component. This can be done by elaborating the UML state diagrams created for the analysis model and by examining all use cases that are relevant to the design class.


# Advantages :
 1. Ease of deployment .
 2. Reduced cost .
 3. Ease of development 
 4. Reusable
 5. Modification of technical complexity
 6. Reliability
 7. System maintenance and evolution
 8. Independent


# What is “Props” and how to use it in React?
![img](https://miro.medium.com/max/1138/1*27LtOtFyJe7MguQkNcZQjQ.png)

1. What is Props?
React is a component-based library which divides the UI into little reusable pieces. In some cases, those components need to communicate send data to each other and the way to pass data between components is by using props.“Props” is a special keyword in React, which stands for properties and is being used for passing data from one component to another.But the important part here is that data with props are being passed in a uni-directional flow,one way from parent to child.props data is read-only, which means that data coming from the parent should not be changed by child components.

# Using Props in React :
1. Firstly, define an attribute and its value(data).
2. Then pass it to child components by using Props.
3. Finally, render the Props Data.

# Recap:
* Props stand for properties and is a special keyword in React
* Props are being passed to components like function arguments
* Props can only be passed to components in one-way (parent to child)
* Props data is immutable (read-only).






  































   





