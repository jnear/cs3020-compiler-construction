# Assignment 4

**Implement a compiler for the `LIf` language by modifying the
`compiler.py` file in the `a4` directory of the [assignments
repository](https://github.com/jnear/cs3020-assignments) and submit
your `compiler.py` file on the course Brightspace under "Assignment
4".**

**Due: Monday, Mar 4, 11:59pm**

Complete `compiler.py` so that it implements a compiler from the
`LIf` language to x86 assembly. A grammar for the required subset
appears below.

**Concrete Syntax:**
```
expr ::= x | n | expr + expr | expr - expr | expr && expr | expr || expr
       | expr == expr | expr > expr | expr < expr | expr >= expr | expr <= expr
stmt ::= x = expr | print(expr) | if expr: stmt+ else: stmt+
LIf ::= stmt*
```

**Abstract Syntax:**
```
op    ::= "add" | "sub" | "not" | "or" | "and" | "eq" | "gt" | "gte" | "lt" | "lte"
Expr  ::= Var(x) | Constant(n) | Prim(op, List[Expr])
Stmt  ::= Assign(x, Expr) | Print(Expr) | If(Expr, Stmts, Stmts)
Stmts ::= List[Stmt]
LIf  ::= Program(Stmts)
```

An online compiler for this assignment is available
[here](http://jnear.w3.uvm.edu/cs3020/compiler-a4.php).

