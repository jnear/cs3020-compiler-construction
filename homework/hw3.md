# Assignment 3

**Implement a compiler for the `LVar` language by modifying the
`compiler.py` file in the `a3` directory of the [assignments
repository](https://github.com/jnear/cs3020-assignments) and submit
your `compiler.py` file on the course Brightspace under "Assignment
3".**

**Due: Tuesday, Feb 18, 11:59pm**

Complete `compiler.py` so that it implements a compiler from the
`LVar` language to x86 assembly. A grammar for the required subset
appears below. Your compiler should perform **register allocation** by
graph coloring.

**Concrete Syntax:**
```
expr ::= x | n | expr + expr
stmt ::= x = expr | print(expr)
LVar ::= stmt*
```

**Abstract Syntax:**
```
op ::= "add"
Expr ::= Var(x) | Constant(n) | Prim(op, [Expr])
Stmt ::= Assign(x, Expr) | Print(Expr)
LVar ::= Program([Stmt])
```

## Online Compiler

An online compiler for this assignment is available
[here](http://jnear.w3.uvm.edu/cs3020/compiler-a3.php).

