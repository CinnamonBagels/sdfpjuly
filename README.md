# sdfpjuly
[presentation](https://docs.google.com/presentation/d/1rNw7aVbKJ5AVBUDOnLrKPRBrNvEN3Pm1N602w_hUAp0/edit?usp=sharing)

Choose one, or do both!

### Calculator
[kata link](https://www.codewars.com/kata/huttons-razor/discuss/haskell)

1. Build an ADT that can represent a mathmatical expression. For starters, your data type may look like this:
```
type Expr =
  Lit Int
  | Add Expr Expr
```

2. Next, write an interpreter that, when passed an ADT as an argument, can output the result
```
function interpret(adt) -> int

interpret Add (Lit 1) (Lit 1) -> 2
```
3. Write a pretty-printer for your new ADT so that people can actually understand it. Surround each Expr in parentheses
```
function pretty(adt) -> String

pretty Add (Lit 1) (Lit 1) -> "(1+2)"
pretty Add (Lit 1) (Add (Lit 2) (Add (Lit 3) (Lit 4))) -> (1+(2+(3+4)))
```

bonus:
* Implement other arithmetic functions (multiplication, division, subtraction, powers)
* Parentheses evaluation

### JSON
Your task is to implement a JSON interpreter that, when given a JSON algebraic data type, will output a String that represents that JSON structure (or literal)

For starters:
```
type JsonNode 
  = JsonBool Bool
  | JsonInt Int
  | JsonObject (Map String JsonNode)
```

```
function interpret(adt) -> String

interpret JsonBool true -> true
interpret ?? -> {"key":"value"}
```

bonus:
* Implement JsonArray
