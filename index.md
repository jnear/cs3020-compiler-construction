---
title: CS 3020: Compiler Construction
layout: default
---

# UVM CS 3020: Compiler Construction (Spring 2024)

## Administrative

- **Lecture**: Monday, Wednesday, Friday, 10:50 - 11:40am, Kalkin 001
- **Instructor**: Joe Near (jnear at uvm dot edu)
- **Office hours**: 9:30am - 10:30am, Monday and Friday, Innovation Hall E458

## Course Description

This course covers the design and construction of compilers. You'll
learn how to translate a high-level, garbage-collected programming
language all the way into Intel x86 assembly language.

Instead of learning about each phase of the compilation process
sequentially, we'll start by compiling a tiny subset of the target
language directly into assembly code. Each week, we'll add a new
feature to our language, and learn about all the phases needed to
compile that feature into assembly. At each step, you'll have a
functioning compiler that can run real code; by the end of the course,
your compiler will work on a realistic programming language including
first-class functions.

Topics covered include:

- representation and analysis of code
- register allocation
- static type checking
- mutable data
- garbage collection
- first-class functions and closure conversion

This course will be structured around lectures and a weekly
programming assignment. Each lecture will cover a new language feature
and the techniques needed to compile it; in the corresponding
programming assignment, you will implement support for the new feature
in your own compiler. Students should expect to spend 6-8 hours per
week outside of class on the weekly programming assignments. The
required materials for this course are all freely available online.

Students will also complete a final project, in which they extend
their compiler with an additional significant language feature of
their choice.

This course is primarily intended for computer science students, but
may also be appropriate for some graduate students in other areas with
an interest in programming languages and strong programming
experience.

## Text and Resources

Please **do not** buy any books for this course. All required reference material is available online for free.

The primary textbook we will use for this course is:

- [Essentials of Compilation](https://github.com/jnear/cs3020-compiler-construction/blob/main/book.pdf)  
  Jeremy Siek.

Other course resources:

- **Announcements** will be posted on the course Brightspace
- **Homework assignments**
  - Descriptions available in the list of assignments below
  - [Download assignment code on the course code repository](https://github.com/jnear/cs3020-assignments)
  - Online compilers are available for each assignment (see links in the assignment description)
  - Turn in homework assignments on Brightspace
- **In-class exercises**
  - [Download notebooks here](https://github.com/jnear/cs3020-assignments/tree/main/exercises)
  - Turn in notebook files on Brightspace


Additional/fun resources:

- Code from lectures is [available on Github](https://github.com/jnear/cs3020-compiler-construction/tree/main/lectures)
- The [midterm review sheet](https://github.com/jnear/cs3020-compiler-construction/tree/main/lectures/midterm-review.md) is available
- The [final review sheet](https://github.com/jnear/cs3020-compiler-construction/tree/main/lectures/final-review.md) is available
- A [complete listing of Python's AST types](https://docs.python.org/3/library/ast.html)
- Fun link: a [list of companies who need compiler developers!](https://mgaudet.github.io/CompilerJobs/)

# Policies

## Grading

Your grade for the course will be determined as follows:

- 7 homework assignments (8% each; 56% total)
- 7 self-review assignments (4% total)
- in-class weekly exercises (20% total)
- final project (10%)
- midterm exam (5%)
- final exam (5%)

Your final grade will be determined by summing the total number of
points awarded and calculating the percentage of the total possible
points. This percentage is translated into a letter grade as follows:

### Undergraduate Students

| Percent | Letter Grade |
| ------: | ------------ |
| 98-100  | A+           |
| 93-97   | A            |
| 90-92   | A-           |
| 87-89   | B+           |
| 83-86   | B            |
| 80-82   | B-           |
| 77-79   | C+           |
| 73-76   | C            |
| 70-72   | C-           |
| 67-69   | D+           |
| 63-66   | D            |
| 60-62   | D-           |
| <60     | F            |

## Assignments

Assignments will generally be due weekly on Mondays at 11:59pm,
with breaks for the midterm exam and final project. Your assignment
will be graded using a test suite which will be made available one day
before the assignment due date.

Late assignments will **not** be accepted. Each assignment builds
extensively on the last one, and mastering the assignment material is
crucial to success in this course. If you fall behind on completing
the assignments, it will be extremely difficult to catch up.

Therefore, on Wednesday after each assignment due date, we will
discuss that assignment's solution in lecture, and the complete
solution will be made available on Brightspace. I encourage students to
take advantage of the official solutions to avoid falling behind.

Partial credit will be (extensively) given on assignments. I encourage
you to submit *something* for every assignment, even if your solution
is far from complete.

Assignments will be graded according to the following rubric:

| Grade | Assignment Status                                         |
| ----: | -------------------                                       |
| 100   | Passes all test cases                                     |
| 95    | Passes 75% of test cases                                  |
| 90    | Passes 50% of test cases                                  |
| 85    | Passes at least 1 test case                               |
| 80    | Project compiles; all passes appear to be nearly complete |
| 75    | All or nearly all passes appear nearly complete           |
| 70    | Significant work on all passes                            |
| 65    | Significant work on at least 75% of the passes            |
| 60    | Significant work on at least half of the passes           |
| <60   | Missing passes                                            |

## Self-Review Assignments

Each homework assignment will have a corresponding *self-review
assignment* due one week later. The self-review assignment is an
opportunity for students to describe and explain the differences
between their solution and the instructor solution.

For each pass of the compiler, your self-review should give short
(1-paragraph) answers for two questions:
- What functionality is missing or broken in your implementation?
- How does your implementation differs from the instructor solution?

If your compiler passes all of the test cases, and correctly
implements the same functionality as the instructor solution, then the
self-review assignment is trivial (the answer to both questions is
"none"), and the self-review assignment is essentially *free points*.

## In-Class Exercise

An *in-class exercise* will be due every Friday at 11:59pm. The
exercises for the week will be released on Monday morning, and we will
complete these exercises together during the lectures each week. If
you attend lectures and follow along, the in-class exercises should
not require significant additional time outside of lecture to
complete.

## Exams

There will be two exams: a midterm and a final. You will be allowed
unlimited pages of notes for each exam. See the schedule below for the dates.

## Final Projects

Each student will select and complete a new language feature for their
compiler. Final project deliverables will consist of a short project
proposal, a compiler implementing the selected language feature, and
test cases demonstrating its use. Final projects may be completed in
teams of up to 3 students; larger teams will be expected to complete
more ambitious projects.

[Click here for more information on final projects](https://jnear.github.io/cs3020-compiler-construction/projects).

## Collaboration & Allowed References

Collaboration on the high-level ideas and approach on assignments is
encouraged. Copying someone else's work (outside of your team
members) is not allowed.

The official references for the course are listed in the schedule
below. Copying from references other than these is not allowed. In
particular, code should not be copied from other sources, including
Stack Overflow and other public sources.

Students caught copying work are eligible for immediate failure of the
course and disciplinary action by the University. All academic
integrity misconduct will be treated according to [UVM's Code of
Academic
Integrity](https://www.uvm.edu/policies/student/acadintegrity.pdf).


# Assignments

| Assignment | Topics Covered                                                                                                    | Text Chapter  | Due Date        |
|-----------:|-------------------------------------------------------------------------------------------------------------------|---------------|-----------------|
|          1 | [Compiling Lmin to x86](https://github.com/jnear/cs3020-compiler-construction/blob/main/homework/hw1.md)          | Chapter 1 & 2 | Jan 22, 11:59pm |
|          2 | [Compiling Lvar to x86](https://github.com/jnear/cs3020-compiler-construction/blob/main/homework/hw2.md)          | Chapter 2     | Feb 5, 11:59pm  |
|          3 | [Register Allocation](https://github.com/jnear/cs3020-compiler-construction/blob/main/homework/hw3.md)            | Chapter 4     | Feb 20, 11:59pm |
|          4 | [Booleans and Control Flow](https://github.com/jnear/cs3020-compiler-construction/blob/main/homework/hw4.md)      | Chapter 5     | Mar 4, 11:59pm  |
|          5 | [Loops & Dataflow analysis](https://github.com/jnear/cs3020-compiler-construction/blob/main/homework/hw5.md)      | Chapter 6     | Mar 25, 11:59pm |
|          6 | [Vectors and Garbage Collection](https://github.com/jnear/cs3020-compiler-construction/blob/main/homework/hw6.md) | Chapter 7     | Apr 8, 11:59pm  |
|          7 | [Compiling Functions](https://github.com/jnear/cs3020-compiler-construction/blob/main/homework/hw7.md)            | Chapter 8     | Apr 22, 11:59pm |
|            | Final Project                                                                                                     |               | *See below*     |

# Class Schedule

**Note: no class on the following dates:**
- Monday, January 15 (MLK day)
- Monday, February 19 (Presidents' day)
- March 11-15 (Spring break)
- April 8 (eclipse day)

**Exams**:
- Midterm exam: Friday, March 8, in class
- Final exam: Monday, May 6, 10:30-11:30am, Kalkin 001

**Extra credit opportunities**: The CS department will host between 6
and 9 invited talks by faculty candidates this semester. If you attend
the talk, take brief notes (1-2 paragraphs summarizing the key
points), and email the notes to me by the next day, I will add 0.25%
of extra credit to your final grade in the course. If you attend all 9
talks, you will receive a total of 2.25% extra credit on your final
grade.

| Week of | Topic                                              | Assignment                                             |
|--------:|----------------------------------------------------|--------------------------------------------------------|
|  Jan 15 | ASTs, Interpreters, x86 Assembly (no class Monday) |                                                        |
|  Jan 22 | Compiling Lmin                                     | A1 Due (Monday)                                        |
|  Jan 29 | Compiling Lvar                                     | A1 Review Due (Monday)                                 |
|   Feb 5 | Register allocation                                | A2 Due (Monday)                                        |
|  Feb 12 | Register allocation                                | A2 Review Due (Monday)                                 |
|  Feb 19 | Booleans & Typechecking (no class Monday)          | A3 Due (**Tuesday**)                                   |
|  Feb 26 | Compiling Lif                                      | A3 Review Due (Monday)                                 |
|   Mar 4 | Compiling Lif (midterm exam Friday)                | A4 Due (Monday)                                        |
|  Mar 11 | *Spring Break* (no class)                          |                                                        |
|  Mar 18 | Loops & Dataflow analysis                          | A4 Review Due (**Tuesday**)                            |
|  Mar 25 | Vectors & Garbage collection I                     | A5 Due (Monday)                                        |
|   Apr 1 | Vectors & Garbage collection II                    | A5 Review Due (Monday)                                 |
|   Apr 8 | Compiling functions (no class Monday)              | A6 Due (Monday)                                        |
|  Apr 15 | Compiling first-class functions                    | A6 Review Due (Monday); Project Proposals Due (Monday) |
|  Apr 22 | Dynamic typing & objects                           | A7 Due (Monday)                                        |
|  Apr 29 | Optimization; binary & instruction sets            | A7 Review Due (Monday); Project Milestone (Monday)     |
|   May 6 | *Finals week* (no class); Final exam (Monday)      | Final Project Due (Monday)                             |
