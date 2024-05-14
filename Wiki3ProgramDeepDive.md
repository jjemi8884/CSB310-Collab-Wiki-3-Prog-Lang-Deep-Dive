(Table of contents will go here)

# Programming Language Deep Dive: C++
### Team Crystallized Ember

## Data Types

## Expressions
    
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
function appears in the header-only, then its definition is outside of the class
in a class interface[1].

Furthermore, C++ uses public and private access modifiers, and in addition to constructors, 
it has destructors that function similarly to the 'delete' operator. They are used 
at the end of an object's lifetime for deallocating memory, returning resources 
and cleaning up any open tasks[1].
    
## Object-Oriented Programming
    
## Exception Handling and Event Handling

## Simple Program example


```
(Code blocks in markdown are done by adding three backticks before and after
the code.)

Write a simple program in your chosen language and include it as a code block in 
your markdown file. Ensure that all topics listed above are represented in your 
program.
```

## Reference List

[1c] R.W. Sebesta, Concepts of Programming Languages, 10th ed. Colorado Springs, 
CO, USA: Pearson Education, Inc., 2012.

[2c-image] "C++ Tutorial", W3 Schools. 
[C++ Tutorial](https://www.w3schools.com/cpp/cpp_operators.asp) 
(accessed may 5, 2024).
