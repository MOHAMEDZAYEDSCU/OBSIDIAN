>[!tip]- The Advantages:
>
>>[!success] Cross platform:
>>- you can program with python in many operating system.
>---
>>[!success] could be used for many purposes.
>
>>[!success] Interpreter:
>>- Python runs on an interpreter system, meaning that code can be executed as soon as it is written. This means that prototyping can be very quick.

>[!caution]- Interpreter & Compiler:
>- different ways to execute code
>---
>>[!danger]- Interpreter:
>>- directly execute instructions without the need to be compiled into machine form.
>>---
>>- Execution:
>>	- line by line and from any point.
>>- Performance:
>>	- slower due to the translation at runtime.
>>- debugging:
>>	- easy, you can execute the code line by line and see the result immediately without the need to compile the entire code first.
>>---
>>- like javascript and php.
>---
>>[!danger]- Compiled:
>>- Compile the code first then run.
>>---
>>- Execution:
>>	- the entire code translated at once then execute.
>>- Preformance:
>>	- faster, because of the translation before executing.
>>- Debugging:
>>	- slower, due to the need to compile the entire code before execute it.

## Syntax:

>[!tip]- TIPS:
>- No need to define a datatype for any variable.
>
>- the type automatically assign to the variable after assign a value to it without specifying.
>
>- the body of the function must be shifted from the header to the right >>.
>
>- you can make a function in anywhere and it wouldn't be executed until you call it.
>
>
>
>- ==#== for comments and there are no multi lines comments, but you can use ``` your comments ``` and the python will ignore it while compilation so technically it is comment ...!!

>[!todo]- Data Types & Casting & Assigning Values:
>- int, float, tuple, string, mapping, boolean, dictionary, list, data, complex ....
>	- int(var) -> for casting to int, the string should be number
>	- str(var) -> converting from int or (float!!?) into string.
>	- float(var) -> for converting to float from int.
>- you can cast the var while reading it from the user using:
>	- x = int(input())  -> you need a variable to store the value. not required.
>---
>---
>- float:
>	- for indicating power of 10
>		- 5e2          ->         5*10^2 = 5*100
>		- 5E2
>		- -32e20
>	- for indicating fractions
>		- 53.21
>		- -4.2
>---
>- complex:
>	- for complex number, r + j
>		- 3 + 2j
>		- 5j
>		- -5j
>---
>>[!tip]- Casting:
>>- converting datatypes to another, str, int, float
>>----
>>- list(var or tuple):
>>	- for converting tuples to list or any variable to list.!
>>----
>>- tuple(list or variable):
>>	- for converting lists to tuple.
>>----
>>- str(var):
>>	- for converting the var into str
>>----
>>- and so on for int & float
>---
>>[!caution]- Different types for assigning values:
>>- x, y, z = 3, 4, 5
>>	- you can define variables in one line.
>>----
>>- x = y = z = "Potato"
>>	- for assign the same value to all variables, you need to use =.
>>- you can extract values form a list and store it in variables like this:
>>	![[Pasted image 20240530011239.png]]
>>----
>>- global (var):
>>	- for calling the global variable by reference in a local function.
>>	- changing the global variable value.
>>	- you can use global variable without type global 'var' but you can't modify it.
>>----

>[!success]- Arithmetic Operations:
>
>- Power by 2 astresks:
>	- 2 ****** 3 > for   2^3 = 8
>----
>- int Division:
>	- by using 2 //
>	- it ignore the fraction and keep the int only.

>[!danger]- Print & Scan:
>- print("the text you want to print..")
>	- it automatically put a new line for each print
>	- with " ", for print the same syntax as entered.
>	- without " ", for print variables if found.
>- print("the comment", variable)
>	- for printing the comment then the variable.
>---
>- print(f"your comment and {variable name} to print them")
>	- using f is instead of .format() function
>
>- print("your comment with {}".format(variable))
>	- the format function work as extent, by ' . '
>	- the format function remove any {} and put the variable
>	- the number of argument = num of {}.
>---
>- print(x, end = "  ")
>	- for printing the variable x and space only, without a new line.
>- print()
>	- for printing a new line.
>---
>>[!tip]- input:
>>- x = input("comment you want")
>>	- the input always be a string, so we need casting.

>[!caution]- Conditions {if, elif, else}:
>
>>[!help] if:
>>- if condition :
>>     _.__body function__._
>>	- you need to make a tap for the function body, it is important that the function body be shifted to right than the head of the condition.
>>	- you need to put ' : ' in the end of the condition.
>---
>>[!success]- elif:
>>- elif condition :
>>	- to perform the function in specific condition.
>---
>>[!todo]- else:
>>
>>     - if the if statement doesn't happened, do else function.
>>     - you can use it in for loop to do anything after the for or while  loop function has ended ==without break==.      ___else: Fnc body___
>----
>>[!]

>[!success]- Lists & Tuples:
>>[!tip]- List:
>>- you can modify and change elements after creating it.
>>- defined using {}
>>---
>>- list = [3 , 4 , 5]
>>	- now this is a list of 3 component.
>>	- the iteration start form 0.
>>---
>>- list.append(var)
>>	- for add a variable(single or list of values) to the list as a single element.
>>----
>>- list.extend(another_list)
>>	- to add the elements of another_list to the list
>>----
>>- del(list[index])
>>	- for deleting element in a specific index
>>----
>>- list.remove(var(single or list))
>>	- it just remove 1 element, but if this one element is a list so it will be delete.
>---
>>[!todo]- Tuple:
>>- you cannot change or modify the elements after creating it.
>>
>>- defined using (), or put ' , ' in the end of the variable.
>>	- x = 5,
>>
>>- more memory efficient and faster.
>>---
>>- tuple(1, 2, 3)
>>	- tuple of 3 component

>[!Failure]- Loops {for, while}:
>
>>[!caution]- For:
>>- for [iteration variable name] in [lists, array of char, range(num)] ==:==  
>>	- you can use multiple iteration variables.
>>	- you declare the variable in for loop and it's value depend on the second part of the for loop variable.
>>		- for example: 
>>			- if we put a list, the {i} will have all the values in the list, strings, character, int ,....
>>			- if we use range(5), {i} will have all values from 0 to 4,   (5 - 1)
>>			- if we use one string, {i} will walk through its characters and will have each character value.
>>		----
>>	  - you can use:  for i in range():
>>		  - for making an infinity loop and put a condition inside to break it using if.
>---
>>[!caution]- While:
>>- while [condition] :
>>	- for the execution of a code multiple times as the a condition says. 
>---
>>[!tip]- Additional Conditions:
>>- continue
>>	- for skip the current iteration and begin from the next one.
>>---
>>- break
>>	- to stop the loop.
>>	- just type it in a line.
>>---
>>- range()
>>	- a function return sequence of numbers, starting from 0 by default, and increments by 1 (by default), and ends at a specified number.
>>	- range (6):
>>		- from 0 to 5
>>	- range (2,8):
>>		- from 2 to 7
>>	- range (2, 30, 3):
>>		- from 2 to 30 and increment by 3 each time.
>>---
>>- pass
>>	- for loop cannot be empty so we use pass in case of non usage of the for loop.
>>---

>[!caution]- Functions:
>- you can use a global variable name inside the function and assign a new value to it as local one without affecting the global variable...
>- use (global var) to change the value of the global variable inside function.
>- you can put boolean condition in return for return true or false.
>	- return num%2 == 0
>----
>- def name(argument):
>     - this is the prototype header of a function in python
>     - ==you need to put ' : ' in the end.==
>     - always use def.
>     - __the function body is shifted to the right >> than the header, instead of {} in C++__.
>----
>

>[!todo]- Built-in Function:
>- type(var)
>	- for knowing the type of a variable var
>---
>- len(string)
>	- for knowing the length of the string s
>---
>- abs(int, complex)
>	- for returning the absolute value.
>---
>>[!caution]- Map
>>- map (function, list-tuple-number-..)
>>	- for perform the function to all the elements in {list, tuple, number} depend on the function variable in the head.
>>	- need a variable to store the results.
>>	- you can display the results as list or tuple...
>>----
>>- ==Example:==
>>		![[Pasted image 20240601162335.png]]
>>		----
>>		![[Pasted image 20240601162822.png]]
>>		----
>>		![[Pasted image 20240601162927.png]]
>----
>
-----------------------
## Logical Operations:

>[!todo]-  _ >, <, >=, <=, !=, == :
>- for set conditions in if for example...
>----
>- 

-----------------------
# Searching Algorithms:

>[!tip]- linear search:
>- go for each element from the begging to the end.
>- O(n)  -> in average and it is worst case.

>[!caution]- Binary Search:
>- used in sorted arrays.
>- begin from the middle interval of the array and split the array into half
>- O {log2(n)}

>[!danger]- Ternary Search