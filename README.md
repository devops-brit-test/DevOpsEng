# Tests for DevOps 
Powershell tasks for DevOps Engineer role. 
## Getting Started
Please create a folder with the task name and place your powershell script inside. For example:
```
task1\task1.ps1
```

## Task 1
The input required for task1 is located at 
```
task1\task1_input.txt
```
Please ensure your script shows the code you used to get the results and outputs of both parts of the task. For example:
```
write-output "result of task1 part a is: x"
```
### Part A
You are on floor 0 of an apartment building and are required to reach a particular floor. The instructions on how to reach the floor are as follows:

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

## Task 2

### Part A
Create a powershell module named 'Task2' which has a function named Get-ServiceDetails.  
The Get-ServiceDetails function must:
* Take pipeline input from the Get-Service cmdlet
* return the name of the services that have the status of 'stopped'
* include the manufacturer and model of the computer the function is run on for each service.

As an example when the following command is run:

```
Get-Service | Get-ServiceDetails | select -first 3
```

The output should look something like this:

```
ComputerName ServiceName    Manufacturer Model
------------ -----------    ------------ -----
ComputerA    AarSvc_2e4fc8a Fabrikam     AdventureWorks
ComputerA    AJRouter       Fabrikam     AdventureWorks
ComputerA    ALG            Fabrikam     AdventureWorks
```

### Part B
Create a script names Task2.ps1 that uses the module created in Part A and:
* Only outputs services with names that start with the letter 'd'
* when the script is run the result can be piped to the Export-csv cmdlet

For example, when the following is run the file task2_results.csv has only services that start with the letter 'd':

```
.\task2\task2.ps1 | Export-csv .\task2\task2_results.csv
```
NB: the task2_results.csv file is not required to be supplied with as part final test files. 
