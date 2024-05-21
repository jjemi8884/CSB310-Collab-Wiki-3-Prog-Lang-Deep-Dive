# Programming Language Deep Dive: C++

### *Team Crystallized Ember*

# Table of Contents

* [Data Types](#data-types)
* [Expressions](#expressions)
* [Assignment Statements](#assignment-statements)
* [Statement-Level Control Structures](#statement-level-control-structures)
* [Subprograms](#subprograms)
* [Abstract Data Types and Encapsulation Concepts](#abstract-data-types-and-encapsulation-concepts)
* [Object-Oriented Programming](#object-oriented-programming)
* [Example Program](#simple-program-example)
* [Reference List](#reference-list)

<br>For our final wiki, we have chosen to cover the C++ programming language. We made 
this selection, in part, because of the popularity of the C-languages, as well as 
C++'s status in the current job market. Below, we discuss several language features, 
including data types, expressions, assignments statements, control structures, subprograms, 
abstract data types and encapsulation, and object-oriented programming. And finally, 
we showcase a simple program, featuring our very own TA, Gabi. Enjoy!

## Data Types
### Author: Rojee Koju

C++ supports a wide variety of data types and the programmer can select the data 
type appropriate to the need of the application. Data types specify the size and 
types of values to be stored. However, storage representation and machine 
instructions to manipulate each data type differ from machine to machine,
although C++ instructions are identical on all machines[1].

<img src=img/Datatype.png width="600"><br>

Data Types in C++ are mainly divided into 3 types:

1.Primary Data Types: These data types are built-in or predefined data types and can be used directly by the users to declare variables. These include
int, char, boolean, floating point, double floating point, valueless or void, wide character.

2.Derived Data Types: Derived Data types that are derived from the primitive or built-in data types are referred to as derived data types. 
These are function, Array, Pointer, Reference.

3.Abstract or User-Defined data Types: These data types are defined by the user itself. These can be class, structure, union and enumeration. 

## Expressions
### Author: Rojee Koju

C++ expression consists of operators, constants, and variables which are arranged according to the rules of the language. It can also 
contain function calls which return values. An expression can consist of one or more operands, zero or more operators to compute a value. 
Every expression produces some value which is assigned to the variable with the help of an assignment operator[2].

<img src=img/Expression.png width="600"><br>

C++ expression consists of Constant, Integral, Float, Pointer, Relational, Logical, Bitwise, Special Assignment Expressions.

Constant expressions:
A constant expression is an expression that includes only constant values. This is an expression whose value is determined at compile time
but evaluated at run time. It can include integer, character, floating-point constants, and enumerations.

Integral Expressions:
An integer expression is an expression that produces the integer value as output after performing all the explicit and implicit conversions.

Float Expressions:
A float expression is an expression that produces floating-point value as output after performing all the explicit and implicit conversions.

Pointer Expressions:
A pointer expression is an expression that produces address value as an output.

Relational Expressions:
A relational expression is an expression that produces a value of type bool, which can be either true or false. It is also known as a 
boolean expression. When arithmetic expressions are used on both sides of the relational operator, arithmetic expressions are evaluated 
first, and then their results are compared.

Logical Expressions:
A logical expression is an expression that combines two or more relational expressions and produces a bool type value. The logical 
operators are '&&' and '||' that combines two or more relational expressions.

Bitwise Expressions:
A bitwise expression is an expression which is used to manipulate the data at a bit level. They are basically used to shift the bits.

Special Assignment Expressions:
Special assignment expressions are the expressions which can be further classified depending upon the value assigned to the variable.

## Assignment Statements
### Author: Cheryl Moser

For simple assignments, C++ uses a single equal sign ("=") as the operator -- 
not to be confused with the double-equal, equality comparison operator ("=="). 
This way of distinguishing between assignment-equals and comparison-equals is the 
same as we are used to seeing in Java. C++ also has ten compound assignment operators. 
These are operators that serve as shorthand for when the left side of the operator 
is also the first operand on the right side. For example, the expressions x = x + 2, 
and x += 2 are synonymous[3].

<img src=img/assignmentW3.png width="600"><br>
<em>[4] Compound Assignment Operator List</em>

Unary assignment operators are valid in C++, and they can serve as negation (-1), 
incrementing (count ++), or decrementing (count --). Placement of the unary increment 
or decrement operator is important, as the expressions “total = count ++,” and 
“total = ++ count” are not the same assignment. In the first expression, count is
first assigned to sum, and then incremented; in the latter, count is incremented
before being assigned to sum[3].

Expressions can be used within an assignment operation, though at the expense of 
readability. Mixed-mode assignments are also supported via implicit and explicit 
conversion rules. C++ conversion rules are less restrictive than Java because widening 
is not a consideration, allowing conversion to be used freely. Multiple assignments 
are not supported in C++.

## Statement-Level Control Structures
### Author: Justin Jemison

<img src=img/BingImageGen.jpg width="600"><br>
<em>Prompt = Java, C, and C++, hanging out in a forest aliens contemplating the setting sun and what it all means</em>
<P>C++ statement level control structures are the evolutionary step between the C language 
and Java; the “For” loop control statement is a prime example. In C, you can define the control 
variable anywhere before the For loop, and you can have multiple control statements within the loop. 
The Scope of the variable is the entire function. C++ created restrictions that any variable 
created in the loop, will have its scope defined in the loop. Java inherited this trait from C++. 
<p>example:
<p>In C programming
<p>int count = 0;
<p>for (count = 1; count < ; count++){
<p>//do something
<p>Goto -> (outside for loop)
<p>}
<p>Print (count);
<p>Output  = 10
<P>The small code above will work in C because you defined the variable (Count) before the for-loop. Whereas in C++, 
you can define the count in the for-loop control statement.
<p>For (int count = 0; count <=10; count++){
<p>//do something.
<p>}
<P></P>
C++ also added the ability to have Boolean operator within the statement. In C this was not available 
and in Java this is the only available option of the second control statement in the For-loop.
C++ also stipulated the rule that the first expression in the For-loop control structure would only run the first time, 
the other two expressions will run each iteration of the loop. The first expression
can also define a variable that can be used to control the loop and will stay within the scope of the For-loop.

Taking a look at the “If”, “then”, “Else", statements C++ allowed an arithmetic  
expression along with a Boolean expression that can be used within the control statement of the “IF” expression.  
Java deviated from this practice and only used Boolean expressions to control IF statements.
The multi-selectors are the same between Java and C++ where they both use the Switch(integer) 
and a separate integer for each case. A Break statement must be used to terminate out of the case statement, 
or cases after the selected case will execute. There is also a “Default” case that can be used. 
C++. Java did take a more restrictive approach in not allowing case expressions outside the top of the body of 
the “Switch” statement. As shown above C++ is the evolution steppingstone from C to Java. It is less restricted 
than Java and has more capabilities than C.

## Subprograms
### Author: Mika Kitazumi
Subprograms, also known as functions or methods, are fundamental building blocks 
in C++. They promote code reusability, modularity, and readability. Subprograms encapsulate 
a specific task or set of instructions that can be called from other parts of your program.
There are two main types of subprograms in C++:
- Functions: Functions are independent blocks of code that perform a specific task. 
They can take zero or more arguments (data passed to the function) and optionally return a value. 
Functions are declared with the return type, followed by the function name and parentheses for arguments.[5]
```
int add(int x, int y) {
return x + y;
}
```
- Member functions: Member functions are functions associated with a class (a user-defined blueprint for creating objects). They operate on the data (member variables) of a specific object and can access both public and private members of the class. Member functions are declared within the class definition.
```
class Point {
public:
int x;
int y;

// Member function to set the coordinates of a point
void setPoint(int x_val, int y_val) {
x = x_val;
y = y_val;
}
};
```
Here are some key benefits of using subprograms:
- Reusability: Subprograms can be called from multiple locations in your code, eliminating the need to duplicate code.
- Modularity: Subprograms break down complex programs into smaller, manageable units, improving code organization and maintainability.
- Readability: Subprograms with descriptive names enhance code clarity and make it easier to understand the program's logic.
By effectively utilizing subprograms, you can create well-structured, efficient, and maintainable C++ programs.

    
## Abstract Data Types and Encapsulation Concepts
### Author: Cheryl Moser

C++ supports abstract data types (ADT) through classes and structs. A struct is 
a type whose definition contains only data fields. For example: a struct for creating 
a point in two-dimensional space would contain two data fields: x and y. A class 
is a type containing data fields (data members), and member functions. Objects of
the class (instances) can access the set of public methods. Member functions of
a class are shared among all instances; however, instances have their own set
of data members[3].

The data members of an object can have different scopes. These include[3]:
- *Static:*  Created with the "static" keyword inside the class definition and 
    referenced directly by name. The lifetime of static members is for the duration
    of the program execution. Static members are shared among class instances.
    
- *Stack dynamic:* Created in the variable declaration inside a function, and 
    also referenced directly. This member exists on the functions stack frame, and
    it is destroyed at the end of function execution.
    
- *heap dynamic:* Declared as a class member, but it is referenced through pointers.
    These members are created with the "new" operator, and they exist until manual
    destruction is performed using the "delete" operator.

Member functions can appear in the class body or in the class header. For cases 
where they appear only in the header, or in both header and body, the function is 
inlined, wherein function code is copied into the calling code. This eliminates
the need for function calls, making the runtime more efficient. If the member
function appears in the header-only, then its definition is outside the class[3].

Furthermore, C++ uses public and private access modifiers, and in addition to constructors, 
it has destructors that function similarly to the 'delete' operator. They are used 
at the end of an object's lifetime for deallocating memory, returning resources 
and cleaning up any open tasks[3].
    
## Object-Oriented Programming
### Author: Mika Kitazumi
Object-oriented programming (OOP) is a fundamental programming paradigm that revolves
around objects.  An object encapsulates data (attributes) and the code that operates 
on that data (methods).  This concept of data hiding promotes modularity, reusability, and
maintainability in C++ programs.

*Key Concepts in OOP*
- Classes: Classes are blueprints that define the properties (attributes) and behavior 
(methods) of objects.  They act as templates for creating objects. A class can contain:

  - Member variables: These variables store the data (attributes) of an object. They can be declared as public, private, or protected, specifying their accessibility to other parts of the program.
  - Member functions: These functions define the behavior of an object. They can access and manipulate the object's member variables.
  - Objects:  Objects are instances of a class.  They represent real-world entities with specific attributes and behaviors.  An object is created using the new operator and calling the class constructor.

- Inheritance:  Inheritance allows new classes (derived classes) to inherit properties and behaviors from existing classes (base classes).  This promotes code reusability and enables the creation of class hierarchies with specialized functionalities.

- Polymorphism:  Polymorphism allows objects of different classes to respond differently to the same method call.  This is achieved through function overloading (having multiple methods with the same name but different parameter lists) and virtual functions (allowing derived classes to override base class methods).

- Encapsulation:  Encapsulation refers to the bundling of data (member variables) and the methods that operate on that data within a class.  This concept promotes data hiding, as member variables can be declared as private, restricting direct access from outside the class.  Methods are used to control access and manipulation of the data.

Benefits of OOP in C++
- Modularity: OOP breaks down complex programs into smaller, manageable units (classes and objects). This 
improves code organization and maintainability.
- Reusability: As mentioned previously, Classes can be reused to create multiple objects, reducing code duplication and development time.
- Data Hiding: Encapsulation protects data integrity by restricting direct access to member variables. Methods provide controlled access to the data, promoting data security.
- Inheritance: Inheritance enables code reuse and promotes code maintainability. Derived classes can inherit from base classes, extending functionality without modifying existing code.
- Polymorphism: Polymorphism allows for flexible and dynamic program behavior. Objects of different types can respond differently to the same method call, improving code flexibility.[6]

A great example of this in action is down below in the coding example.
## Exception Handling and Event Handling
### Author: Justin Jemison 
<img src=img/2023_01_MicrosoftTeams-image-8.jpg width="600"><br>
Standardized and accepted by ANSI in 1990, exception handling for C++ was the first C language 
to have such a structure for error detection. Java also adopted the error handling from C++.
C++ introduced the reserved word “Try” where the scope of an exception was limited to the try {} 
block. The Catch statement would also grant programmers the ability to stop a run time error by 
“catching the error or exception.” This allowed programmers to take action to correct the error 
 in the program and stop it from crashing the program. C++ also allowed programmers to use the “Throw” 
clause that will allow the programmer to dictate when an exception can be thrown. C++ only allowed user 
defined exceptions. There is a default except called the “unexpected” exception, it is not very descriptive and does
not assist in troubleshooting where a problem may be. There are libraries that have 
been created with exceptions installed. For example, the Math library has the exception overflow error.
Java took what C++ was doing with exception handling and expanded upon it creating the Throwable class.
This keeps with the C++ design but uses a more Object-Oriented approach.

## Simple Program example
### Author: Team Crystallized Ember

```
#include <iostream>
#include <string>
using namespace std;

class Faculty{
  public:
    string name;
    string course;
    int salary = 1000000000;
};

class TA: public Faculty{
  public:
    string hours = "Office hours: 24/7/365";
    bool isAvailable = true;

    //Method to update availability
    void updateAvailability(bool availability){
      isAvailable = availability;
    }
    
    //Method to give a raise by a percentage
    int giveRaise(float percentage){
      int raise = static_cast<int>(salary *(percentage/100));
      salary += raise;
      return raise;
    }
};

int main() {
  
  TA t;
  t.name = "Gabi";
  t.course = "Programming Languages";

  //Giving a raise of 5% to the TA
  int raise = t.giveRaise(5.0f);

  int gabiInspiredComputerScienceStudentsWithEasyProblems = 3;

  //define the tolerance of a TA 
  int gabiToleranceFactor = 0;
  int howManyTimesToExplainTheSameIssueUntilUnderstood = 15;
  for(int issue = 0; issue < gabiInspiredComputerScienceStudentsWithEasyProblems ; issue++)
    {
        int gabiCorrectedTheStudentsWayOfThinking = 2; //used as boolean 
        while(gabiCorrectedTheStudentsWayOfThinking)  //just like java :P)
        {
            //see if we solved the issue yet
            howManyTimesToExplainTheSameIssueUntilUnderstood--;
            if(howManyTimesToExplainTheSameIssueUntilUnderstood < 1)
            {
                //break out of while loop
                gabiCorrectedTheStudentsWayOfThinking = 0;
              
            } else {
                gabiToleranceFactor++;
            }
        }
    }

  //Updating availability status
  if(gabiToleranceFactor > 10)
  {
    t.updateAvailability(false);
  }
  
  std::cout << t.name << ": TA, " << t.course << "\nSalary: " << t.salary << " dollars!\n" << t.hours << "\nRaise:" << raise << " dollars!\n" << "Availability: " << (t.isAvailable ? "Available" : "Not available") ;
}
```

## Reference List

[1] "C++ Data Types" https://www.geeksforgeeks.org/cpp-data-types/# (accessed May 16, 2024).

[2] "C++ Expression" https://www.javatpoint.com/cpp-expression (accessed May 16, 2024).

[3] R.W. Sebesta, Concepts of Programming Languages, 10th ed. Colorado Springs, 
CO, USA: Pearson Education, Inc., 2012.

[4] "C++ Tutorial", W3 Schools. 
[C++ Tutorial](https://www.w3schools.com/cpp/cpp_operators.asp) 
(accessed May 5, 2024).

[5]“C++ OOP (Object-Oriented Programming),” www.w3schools.com. https://www.w3schools.com/cpp/cpp_oop.asp

[6] J.Cortadella et al. "Introduction to Programming (in C++) Subprograms:procedures and functions". Dept. CS, UPC
