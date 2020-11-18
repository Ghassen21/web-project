
# Iteration in JavaScript: While and For loops

## What is Loop ?

Consider we need to print “hi” 5 times. If we don’t have loop , what we would be doing is

	console.log("hi");
	console.log("hi");
	console.log("hi");
	console.log("hi");
	console.log("hi");


But , if we know how to use loop , then we can simplify the above code to

	for(var i = 1; i <= 5; i++) {
		console.log('👋');
	}

Looping is a way of executing the same function repeatedly. In other words, loops are used to execute the same block of code again and again, until certain condition is met.


## For Loop


The **for loop** is one of the most common ways to perform repetitive code. It is used when you need to run the same code over and over. For instance, if you have an array of names and want to print a welcome message for each name, then you would use it. You use this look when no pre-condition needs to exist for the loop to run. A for loop syntax is made of three statements.


### Syntax

	for(initialValue; condition; step or increment) {
		// operation
	}


Example .


	for(var i = 0 ;i < 5; i++) {
		console.log(i);
	}

  

**NOTE: The increment does not have be ++, but you’ll see that most commonly.**

### Structure
In the above code

-   **initialValue**  →`i = 0` → Will be executed at the beginning of the loop
-   **condition** →  `i < 5` → is checked every-time before the body of the loop is executed
-   **operation**  → console.log(i) ; → body of the loop
-   **step/increment**  →  `i++`  → Executed every-time after each iteration.

---

Let’s breakdown how it works:

At the beginning of the for loop

	i = 0 ; is initialised

  

First Iteration

	i < 5 is true since i is equal to 0
	i is printed

After end of first iteration

	i = i + 1 is executed

Second iteration

	i < 5 is true since i is equal to 1
	print i

This will be repeated until the condition becomes false.

**A simpler example would be the following:**

	for (var i = 0; i < 2; i++) {
		console.log(i);
	}

Breaking it down:

	// initial Value
	var i = 0

	// if condition → execute body
	if (0 < 2) → true → log(1)

	// increment
	i = i+1;
---
	i = 1;

	// if condition → execute body
	if (1 < 2) → true → log(1)

	// increment
	i = i+1;
---
	i = 2;

	// if condition → execute body
	if (2 < 2) → false→ loop terminated


### For loop implementation with arrays


Consider this array.

	var names = ["James",
		"Jacob",
		"Jackson",
		"Jordan",
		"Jared",
		"Jude",
		"Jeremiah",
		"James"
	];

  

Arrays have a zero-based index, the initial value of a loop counter must be set to zero when iterating through one to avoid going out of bound which causes an error. If you’re just looping through a block of code without an array, then you can set the initial value to whatever suits your needs. To print a greeting message for each name, you can use a for loop to do that.


	for (var index = 0; index < names.length; index++) {
		console.log("Welcome " + names[index]);
	}


## While Loop


The while loop runs a block of code as long as the conditional statement is true. Its syntax is as follow:


	while (condition) {
		// code goes here...
	}


The while loop has lower overhead between the two iteration structures. The loop consists of the keyword while followed by an expression and curly braces. The contents of the loop — what is between the curly braces — are executed as long as the expression evaluates to true.


	while(count < 10) {
		console.log(count);
	}


Now, the example above is incomplete because a while loop needs a way to eventually exit the loop. Normally, this is done by modifying the variable in the expression.


	var count = 1;
	while(count < 10) {
		console.log(count);
		count++;
	}


In while loop we have only space for checking condition .


	var i = 0;
	while(i < 5) {
		console.log(i);
		i = i + 1;
	}

	//output
	1,2,3,4,5


If we forgot the increment then it will result in infinite loop


	var i = 0;
	while(i < 5) {
		console.log(i);
	}


In the above code the value of i will always 0 , so the loops run infinitely .


## When to Use Each Loop

Deciding which loop to use is ultimately a judgment call. Especially as a beginner, don’t let this opinion sway you away from what’s comfortable for your own eyes.


There are other more advanced iteration structures that you can eventually grow to learn, so don’t get hung up deciding between these two.


With that said, a universal rule for choosing between a while loop and for loop is that we use while loops when **we do not know the number of iterations ahead of time** and for loops when **we do know**.


Let’s go through a few examples of each:

- Use a for loop to iterate over an array.

- Use a for loop when you know the loop should execute n times.

- Use a while loop for reading a file into a variable.

- Use a while loop when asking for user input.

- Use a while loop when the increment value is nonstandard.


## More ressources:

[JavaScript Loops Pt.1: Regular For Loops.](https://medium.com/@dallasbille/regular-javascript-for-loops-part-1-76bab795f4c8)


[Javascript “while” Loops](https://medium.com/@dallasbille/javascript-while-loops-pt-4-b9c06527d9d7)

## Summary

![Diagram](diagram-01.jpg)