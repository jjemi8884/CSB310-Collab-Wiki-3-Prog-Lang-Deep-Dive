(Table of contents will go here)

# Programming Language Deep Dive: C++

### *Team Crystallized Ember*

## Data Types

C++ supports a wide variety of data types and the programmer can select teh data 
type appropriate to the need of the application. Data types specify the size and 
types of values to be stored. However, storage representation and machine 
instructions to manipulate each data type differ from machine to machine,
although C++ instructions are identical on all machines[1].

<img src=img/Datatype.png width="600"><br>

Data Types in C++ are mainly divided into 3 types:

1.Primary Data Types: These data types are built-in or predefined data types and can be used directly by the users to declare variables. These include
int, char, boolean, floating point, double floating point, valueless or void, wide character.

2.Derived Data Types: Derived Data types that are derived from the primitive or built-in datatypes are referred to as derived data types. 
These are function, Array, Pointer, Reference.

3.Abstract or User-Defined data Types: These data types are defined by the user itself. These can be class, structure, union and enumeration. 

## Expressions

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
and x += 2 are synonymous[1].

<img src=img/assignmentW3.png width="600"><br>
<em>[2c] Compound Assignment Operator List</em>

Unary assignment operators are valid in C++, and they can serve as negation (-1), 
incrementing (count ++), or decrementing (count --). Placement of the unary increment 
or decrement operator is important, as the expressions “total = count ++,” and 
“total = ++ count” are not the same assignment. In the first expression, count is
first assigned to sum, and then incremented; in the latter, count is incremented
before being assigned to sum[1].

Expressions can be used within an assignment operation, though at the expense of 
readability. Mixed-mode assignments are also supported via implicit and explicit 
conversion rules. C++ conversion rules are less restrictive than Java because widening 
is not a consideration, allowing conversion to be used freely. Multiple assignments 
are not supported in C++.

## Statement-Level Control Structures
### Author: Justin Jemison

<img src=img/BingImageGen.jpg width="600"><br>
<em>[2c] promp = Java, C, and C++, hanging out in a forest aliens contemplating the setting sun and what it all means</em>
<P>C++ statement level control structures are the evolutionary step between the C language 
and Java; the “For” loop control statement is a prime example. In C you can define the control 
variable anywhere before the For loop and you can have multiple control statement within the loop. 
The Scope of that variable is the entire function. C++ created restriction that any variable 
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
<P>The small code above will work in C because you have defined the outside. Where at in C++ 
you can define the count in the for-loop statement itself.
<p>For (int count = 0; count <=10; count++){
<p>//do something.
<p>}
<P></P>
C++ also added the ability to have Boolean within the statement. In C this was not available 
and in Java this is the only available option of the second statement in the “For” loop control statement.
Another think that C++ did was to only ren the first expression in the “For” loop constructor 
at the beginning and then run the other expressions each iteration of the loop. The first expression
can also define a variable that can be used to control the loop and will stay within the scope of the for-loop.

Taking a look at the “If” “then” “Else statement, C++ allowed, just like the “for” statement, an arithmetic  
expression along with a Boolean expression can be used within the control statement of the “IF” expression.  
Java deviated from this practice and only uses Boolean expressions to control IF statements.
The multi-selectors are the same between Java and C++ where they use the Switch(integer) and each case is a 
different integer (case ..) and a Break statement has to be used to not execute the cases after the selected case. 
There is also a “Default” case that can be used. C++. Java did take a more restrictive approach in not allowing 
case expressions outside the top of the body of the “Switch” statement.
As shown above C++ is the evolution steppingstone from C to Java. It is less restricted than Java and has more 
capabilities than C.

## Subprograms
    
## Abstract Data Types and Encapsulation Concepts

### Author: Cheryl Moser

C++ supports abstract data types (ADT) through classes and structs. A struct is 
a type whose definition contains only data fields. For example: a struct for creating 
a point in two-dimensional space would contain two data fields: x and y. A class 
is a type containing data fields (data members), and member functions. Objects of
the class (instances) can access the set of public methods. Member functions of
a class are shared among all instances; however, instances have their own set
of data members[1].

The data members of an object can have different scopes. These include[1]:
- *Static:*  Created with the "static" keyword inside the class definition and 
    referenced directly by name. The lifetime of static members is for the duration
    of the program execution. Static members are shared among class instances.
    
- *Stack dynamic:* Created in the variable declaration inside of a function, and 
    also referenced directly. This member exists on the functions stack frame, and
    it is destroyed at the end of function execution.
    
- *heap dynamic:* Declared as a class member, but it is referenced through pointers.
    These members are created with the "new" operator, and they exist until manual
    destruction is performed using the "delete" operator.

Member functions can appear in the class body or in the class header. For cases 
where they appear only in the header, or in both header and body, the function is 
inlined, wherein function code is copied into the calling code. This eliminates
the need for function calls, making the runtime more efficient. If the member
function appears in the header-only, then its definition is outside of the class[1].

Furthermore, C++ uses public and private access modifiers, and in addition to constructors, 
it has destructors that function similarly to the 'delete' operator. They are used 
at the end of an object's lifetime for deallocating memory, returning resources 
and cleaning up any open tasks[1].
    
## Object-Oriented Programming
    
## Exception Handling and Event Handling
### Author: Justin Jemison 
<img src=img/2023_01_MicrosoftTeams-image-8.jpg width="600"><br>
Standardized and accepted by ANSI in 1990, exception handling for C++, was the first C language 
to have such a structure for error detection. Java also adopted the error handling form C++ along 
with other syntax as listed in statement level control section. C++ introduced the reserved word 
“Try” where the scope of an exception was limited to the try {} block. The Catch statement would 
also grant programmer the ability to stop a run time error by “catching the error or exception” 
and along the programmer to take action to current the error in program and stop it from crashing.
C++ also included a “Binging” exception that can be used with the “Throw” clause that will allow the
programmer to dictate when an exception can be thrown. C++ only allowed user defined exceptions 
except for the “unexpected” exception which is not very descriptive. There are libraries that have 
been created with exceptions installed. For example, the Math library has the exception overflow error.
Java took was C++ was doing with exception handling and expanded upon it creating the Throwable class.
This keeps with the C++ design but used a more Object Oriented approach.

## Simple Program example

### Author(s): Cheryl Moser

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
  
  int gabiInspiredComputerScienceStudentsWithEasyProblems = 10;

  //define the tolerance of a TA 
  int GabiToleranceFactor = 0
  for(int issue = 0; issue < gabiInspiredComputerScienceStudentsWithEasyProblems ; issue++)
    {
        int gabiCorrectedTheStudentsWayOfThinking = 1; //used as boolean 
        while(gabiCorrectedTheStrudentsWayOfThinkig)  //just like java :P)
        {
            //get a responce if the problem was solved
            std::cin >> responce;
            if(responce > 0)
            {
                //break out of while loop
                gabiCorrectedTheStudentsWayOfThinking = 0;
            } else {
                gabiToleranceFactor++;
            }
        }
    }
    

  //Updating availability status
  if(gabiToleranceFactor > 15)
  {
    t.updateAvailability(false);
  }
   
  std::cout << t.name << ": TA, " << t.course << "\nSalary: " << t.salary << " dollars!\n" << t.hours << "\nRaise:" << raise << " dollars!\n"
   << "Availability: " << (t.isAvailable ? "Available" : "Not available") ;
}
```

## Reference List

[1c] R.W. Sebesta, Concepts of Programming Languages, 10th ed. Colorado Springs, 
CO, USA: Pearson Education, Inc., 2012.

[2c-image] "C++ Tutorial", W3 Schools. 
[C++ Tutorial](https://www.w3schools.com/cpp/cpp_operators.asp) 
(accessed may 5, 2024).

[1R] "C++ Data Types" https://www.geeksforgeeks.org/cpp-data-types/# (accessed May 16, 2024).

[2R] "C++ Expression" https://www.javatpoint.com/cpp-expression (accessed May 16, 2024).