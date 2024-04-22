# Notes from chapter 9
## Overview
- **Main Focus**: The chapter discusses the lifecycle of objects in Java, including their creation, management, and destruction within the Java memory model.
- **Key Concepts**: Constructors, garbage collection, memory management (heap and stack), and object lifecycle.
## Object Creation and Constructors
- **Object Creation**: Objects in Java are created using constructors, which are special methods called when a new object instance is created.
- **Constructors**: These are used not only to create objects but also to initialize object state. Constructors can be overloaded to provide different ways of initializing objects based on different inputs.
## Memory Management
- **Heap and Stack:**
  - **Heap**: This is where Java objects reside. The heap is a runtime data area from which memory for all class instances and arrays is allocated.
  - **Stack**: This area stores method calls and local variables. Each thread in Java has its own stack, created when the thread is created.
## Scope and Lifetime of Variables
- **Local Variables**: These live only within the method that declared them. Once the method execution is complete, these variables are no longer accessible.
- **Instance Variables**: These live as long as the object to which they belong remains alive. They are stored in the heap.
## Garbage Collection
- **Process**: Java does not require explicit deallocation of memory. Instead, it uses a garbage collector to automatically manage memory. When objects are no longer in use (i.e., no references to them exist), the garbage collector can reclaim their memory.
- **Abandonment**: Developers do not destroy objects manually; they simply remove all references to the object. Once an object is abandoned, it becomes eligible for garbage collection.
## Practical Tips
- **Efficient Memory Use**: The chapter advises on efficient memory use, such as reusing objects when possible and minimizing the scope of variables to reduce memory overhead.
- **Null References**: Setting object references to null can help in making objects eligible for garbage collection sooner, thus freeing up memory.
## Warning
- The chapter humorously warns readers not to get too attached to objects due to their transient nature in memory, highlighting the importance of understanding object lifecycle for effective Java programming
# Notes from chapter 10
## Overview
- **Purpose**: Understanding the significance and usage of static methods, static variables, and Java's built-in Math class.
## Math Methods and Static Usage
- **Static Methods**: Java’s Math class provides static methods that you can use directly without creating an instance of the class. Examples include Math.sqrt() for square roots and Math.cos() for cosine.
- **Global Accessibility**: Since these methods are static, they are accessible globally, using the class name.
## Static vs. Non-Static Methods
- **Definition and Differences**: Static methods belong to the class rather than an instance, meaning they can be called without creating an object. They cannot access instance variables or methods directly.
## Implications of Static Methods
- **Limitations**: Static methods cannot use non-static (instance) fields or call non-static methods directly.
## Static Variables
- **Shared Value**: Static variables hold a value that is shared among all instances of the class.
- **Example**: A static variable could be used to count the number of instances of a class.
## Static Initialization
- **Purpose**: Static variables can be initialized in static blocks that execute when the class is loaded.
- **Usage**: Useful for complex initialization that static declarations cannot handle.
## Constants (static final)
- **Immutable Constants**: Declaring a variable as static final makes it a constant, meaning it cannot be changed after initial assignment.
- **Usage Example**: Constants like 'Math.PI' are declared as 'static final'.
## Wrappers and Autoboxing
- **Autoboxing**: Java automatically converts between primitive types (like int) and their corresponding object wrapper classes (like 'Integer').
- **Utility Methods**: Wrapper classes include static methods useful for parsing strings to numbers, such as 'Integer.parseInt()'.
## Formatting Numbers and Strings
- **Formatting Tools**: Methods like printf and String.format allow for formatted output, including setting precision for floating-point numbers and formatting dates.
- **Locale-Specific Formats**: These methods can also adapt the output to fit locale-specific conventions.
## Dates and Times
- **Calendar Usage**: Java provides Calendar and other time-managing classes that offer methods to manipulate dates and times, including adding or subtracting time units.
- **Formatting Dates**: Classes like SimpleDateFormat allow for formatting dates into readable strings.
## Static Imports
- **Simplifying Access**: Static imports can be used to access static methods and variables of a class directly without class qualification.
## Best Practices and Tips
- **Appropriate Use**: Use static elements when it makes logical sense for the data or behavior to belong to the class rather than instances.
- **Caution in Usage**: Overusing static can make testing difficult and lead to less flexible code due to the global state it introduces.
