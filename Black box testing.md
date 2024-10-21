## What is blackbox testing?
- A blackbox:
	- You have 0 clue what's inside it. How it's designed/developed and how the error is handled are not known to you
	- You have to test based on **HOW IT BEHAVES**
## Blackbox vs Whitebox
- Blackbox: **TESTING FEATURE**
	- Behavior testing
	- You are testing based on the specifications and comparing it on the output to see how it works
	- Unit test:
		- Testing based on each module
	- Integration test
		- Testing based on a set of modules
	- System test
		- Testing based on the whole system
- Whitebox: **TESTING ARCHITECTURE**
## Equivalence Class Partitioning
- Splitting the input into sets of equivalent classes
- An equivalent class is:
	- A list of data that allows the system to behave the same
	- A list of data in a class that is equivalent
- All data in an equivalent class should gives out an output that behaves the same.
$\Rightarrow$ Don't need to test all values in that class. Only need a representative value.

