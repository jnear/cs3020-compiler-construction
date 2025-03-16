# Assignment 5

**Implement a compiler for the `LWhile` language by modifying the
`compiler.py` file in the `a5` directory of the [assignments
repository](https://github.com/jnear/cs3020-assignments) and submit
your `compiler.py` file on the course Brightspace under "Assignment
5".**

**Due: Monday, Mar 24, 11:59pm**

Complete `compiler.py` so that it implements a compiler from the
`LWhile` language to x86 assembly. A grammar for the required subset
appears below.

**Concrete Syntax:**
```
expr ::= x | n | expr + expr | expr - expr | expr * expr | expr && expr | expr || expr
       | expr == expr | expr > expr | expr < expr | expr >= expr | expr <= expr
stmt ::= x = expr | print(expr) | if expr: stmt+ else: stmt+ | while expr: stmt+
LIf ::= stmt*
```

**Abstract Syntax:**
```
op    ::= "add" | "sub" | "mul" | "not" | "or" | "and" | "eq" | "gt" | "gte" | "lt" | "lte"
Expr  ::= Var(x) | Constant(n) | Prim(op, List[Expr])
Stmt  ::= Assign(x, Expr) | Print(Expr) | If(Expr, Stmts, Stmts) | While(Expr, Stmts)
Stmts ::= List[Stmt]
LIf  ::= Program(Stmts)
```

An online compiler for this assignment is available
[here](http://jnear.w3.uvm.edu/cs3020/compiler-a5.php).

