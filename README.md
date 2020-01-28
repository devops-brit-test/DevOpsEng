# Tests for DevOps 
Puzzles and questions for DevOps Engineer role. 
## Getting Started
For scripting puzzles please create a folder with the puzzle name and place your powershell script inside. For example:
```
puzzle1\puzzle1.ps1
```

## Puzzle 1
The input for puzzle1 is located at 
```
puzzle1\input1.txt
```
Please ensure your script outputs both parts of the puzzle. For example:
```
write-output "result of part a is: x"
```
### Part A
You are on floor 0 of an apartment building and need to reach a particular floor. The instructions on how to reach the floor are as follows:

* An opening parenthesis '(' means you should go up one floor.
* A closing parenthesis ')' means you should go down one floor.

For example:

    (()) and ()() both result in floor 0.
    ((( and (()(()( both result in floor 3.
    ))((((( also results in floor 3.
    ()) and ))( both result in floor -1 (the first basement level).
    ))) and )())()) both result in floor -3.

To what floor do the instructions take you?

### Part B

Given the same instructions, find the position of the first character that causes you to enter the basement (floor -1). The first character in the instructions has position 1, the second character has position 2, and so on.

For example:

    ) causes you to enter the basement at character position 1.
    ()()) causes you to enter the basement at character position 5.

What is the position of the character that causes you to first enter the basement?