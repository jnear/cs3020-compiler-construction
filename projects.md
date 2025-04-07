# Final Projects (Spring 2025)

## Suggested Project Ideas

Each of these project ideas will be discussed in lecture, and textbook
chapters are available for some of them.

### Dataclasses (Simple Object System)

Extend the tuples present in Lfun to *records* with *named fields*,
exposed as classes in the language. There is no chapter in the
textbook describing this extension, but we'll discuss it in class.

<!-- **An online compiler is available [here](https://jnear.w3.uvm.edu/cs202/compiler-dataclasses.php).** -->

Example:

```
class Point:
  x: int
  y: int

def add_point(self: Point, other: Point) -> Point:
    return Point(self.x + other.x, self.y + other.y)

p1 = Point(1, 2)
p2 = Point(3, 4)
p3 = add_point(p1, p2)
```

<!-- ### Functions -->

<!-- Extend the Lfun language to support function definitions. We will -->
<!-- discuss this option in class, and the textbook describes the changes -->
<!-- in Chapter 7. -->

<!-- **An online compiler is available [here](https://jnear.w3.uvm.edu/cs202/compiler-functions.php).** -->

<!-- ``` -->
<!-- def fact(n: int) -> int: -->
<!--     if n == 0 or n == 1: -->
<!--         return 1 -->
<!--     else: -->
<!--         return n * fact(n-1) -->

<!-- print(fact(5)) -->
<!-- ``` -->

### Nested, Lexically-scoped Functions

Extend the Lfun language to support *lexically-scoped functions* via `def`. 
We will discuss this option in class, and the textbook
describes the changes in Chapter 9. Support for `lambda` expressions
is optional (anonymous functions), and more challenging due to changes in the parser.

Example:

```
def f() -> int:
    x = 5
    def g() -> int:
        return x
    return g

print(f()())
```

### Dynamic Typing

Extend the Lfun language to support *dynamic typing* as described in
Chapter 9 of the textbook.

Example:

```
if 5 == 6:
    x = True
else:
    x = 42
```

## Other Project Ideas

  * arrays with non-statically-known indexing (runtime checking)
  * objects with dynamic dispatch
  * objects with inheritance
  * objects with class definitions
  * placing tuple-valued variables in registers
  * lists
  * recursive datatypes / algebraic datatypes
  * optimizations
    * removing unneeded moves
    * removing unneeded jumps
    * removing unneeded tmp vars
  * new data types
    * floating point numbers
    * strings

More complicated:

  * manually-allocated heap data (malloc/free)
  * reference-counted heap data
  * lazy evaluation
  * procedure inlining
  * continuations, exceptions
  * I/O
  * foreign function interface

Very tough: 

  * self hosting
  * macros
  * alternative garbage collector
  * multi-threading, fork join, futures, implicit parallelism

## Requirements

The goal of the final project is for you to design and implement your own compiler extension. Final projects will be completed in groups of 1-3. Your project should be similar in size and scope to a single homework assignment. For groups of size >1, the project should be similar in size and scope to one homework assignment for *each* group member. The deliverables for the project will be as follows:

- A *project proposal* of 1 paragraph, describing:
  - Who is in your group
  - A description of your desired compiler feature (language feature or compiler extension - e.g. "add objects and class definitions with inheritance")
  - A description of the *most scaled-back feasible version* of your compiler feature - e.g. "use vectors containing values and functions to represent objects")
  - A representative test case to demonstrate your new feature
- Your *implementation*, as an extension to the course compiler
  - Include at least 10 representative test cases demonstrating your new feature
- A *README* of at most 1 page, describing the approach you took in your implementation, and features you planned but did not implement
- A *project presentation* of about 5 minutes, including
  - A description of the new feature, including a test case
  - Your implementation approach
  - A description of challenges you encountered / parts you were not able to implement
  - You will submit a video of your project presentation at the same time as your project implementation and README

For the *project milestone*, you should submit:
- A *status update* of 1 paragraph, stating what you have accomplished and what is left to finish
- A file containing your current implementation - either `compiler.py` if you didn't modify any other files, or a .zip file containing the whole compiler directory if you did

## Schedule & Grading

The final project is worth 10% of your final grade. The schedule for final project deliverables, and the contribution of each one to the grade you receive for the final project, are as follows:

|                Deliverable | Due Date                    | Grade Percent | Turn In     |
|---------------------------:|-----------------------------|---------------|-------------|
|           Project Proposal | Monday, Apr 14 at 11:59pm   | 10%           | Brightspace |
|          Project Milestone | Monday, Apr 28 at 11:59pm   | 10%           | Brightspace |
|    Implementation & README | Wednesday, May 7 at 11:59pm | 50%           | Brightspace |
| Project Presentation Video | Wednesday, May 7 at 11:59pm | 30%           | Brightspace |


