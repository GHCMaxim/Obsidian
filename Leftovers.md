
### On the Subject of Access Modifiers

|                                 | Default | Private | Protected | Public |
| ------------------------------- | ------- | ------- | --------- | ------ |
| Same class                      | Yes     | Yes     | Yes       | Yes    |
| Same package                    | Yes     | No      | Yes       | Yes    |
| Different package subclass      | No      | No      | Yes       | Yes    |
| Different package, non-subclass | No      | No      | No        | Yes    |
Essentially speaking:
- Default is no declaration.
- Use `private` for things only in that class
- Use `protected` for things within the class and its subclasses
- Use `public` for things *everywhere*
### On the Subject of Abstractions:
`abstract` is a *non-access modifier*. Which means you have to inherit it to access it. This also means its entire point is to be an *empty piece of code for you to modify in other classes inheriting it.*

Example(taken straight from w3 because I am lazy):
```Java
abstract class Animal {
  // Abstract method (does not have a body)
  public abstract void animalSound();
  public void sleep() {
    System.out.println("Zzz");
  }
}

class Pig extends Animal {
  public void animalSound() {
    System.out.println("The pig says: wee wee");
  }
}

class Main {
  public static void main(String[] args) {
    Pig myPig = new Pig(); 
    myPig.animalSound();
    myPig.sleep();
  }
}
```

### On the Subject of Methods
#### Method Overloading:
This means you are dealing with the possibility of $\geq$ 2 classes with the same name, with different argument.

Example:
```Java
int add(int a, int b){
	return a+b;
}
int add(int a, int b, int c){
	return a+b+c;
}
```

#### Method Overriding:
This means you are dealing with the possibility of 2 methods taking in the same arguments, but different implementation, likely through inheritance. You can use `@Override` to force proper overriding of a method at compile time, but it is unnecessary.

Example:
```Java
class Me {
	void readLetter(String a){
		// do something
	}
}

class Mi extends Me {
	@Override
	void readLetter(String a){
		// do something
	}
}

```

### On the Subject of Sorting Algos
- Bubble and Insertion is best when array is pre-sorted, worst when array is reverse-sorted.
- Quick Sort: Worst when array is sorted or reverse sorted.
- Radix Sort: k is the max digits of an array
- Count Sort: k is size of array
- Bucket Sort: k is number of buckets

| Sorting Algorithm |               | Time Complexity |               | Space Complexity |
| ----------------- | ------------- | --------------- | ------------- | ---------------- |
|                   | Best Case     | Average Case    | Worst Case    | Worst Case       |
| Bubble Sort       | $O(n)$        | $O(n^2)$        | $O(n^2)$      | $O(1)$           |
| Selection Sort    | $O(n^2)$      | $O(n^2)$        | $O(n^2)$      | $O(1)$           |
| Insertion Sort    | $O(n)$        | $O(n^2)$        | $O(n^2)$      | $O(1)$           |
| Merge Sort        | $O(n*log(n))$ | $O(n*log(n))$   | $O(n*log(n))$ | $O(n)$           |
| Heap Sort         | $O(n*log(n))$ | $O(n*log(n))$   | $O(n*log(n))$ | $O(1)$           |
| Quick Sort        | $O(n*log(n))$ | $O(n*log(n))$   | $O(n^2)$      | $O(log(n))$      |
| Radix Sort        | $O(n * k)$    | $O(n * k)$      | $O(n * k)$    | $O(n + k)$       |
| Count Sort        | $O(n + k)$    | $O(n + k)$      | $O(n + k)$    | $O(k)$           |
| Bucket Sort       | $O(n + k)$    | $O(n + k)$      | $O(n^2)$      | $O(n)$           |
### On the Subject of Type Conversion

Type Conversion in Java is like building a house. You building more of the house is free and is done automatically, you break down the house requires explicit permissions. Generally speaking, remember this list, going from smallest to biggest:

Byte $\leftrightarrow$ Short $\leftrightarrow$ Int $\leftrightarrow$ Long $\leftrightarrow$ Float $\leftrightarrow$ Double

#### Widening(Automatic Conversion)
Data types automatically converted when:
- Two data types are compatible
- We assign smaller data type to bigger data type
Example:
```Java
int i = 100;
long l = i;
float f = l;
```
This is automatic, and does not need explicit type casting.

#### Narrowing(Explicit Conversion)

This happens when we *explicitly* want a value of a larger data type turned into a smaller one, so we have to be explicit about the conversion.

Example:
```Java
double d = 100.0;
long l = (long)d;
int i = (int)i
```
Of course, you will lose the fractional part. Considered it floored to save the headache.

### On the Subject of SDLC

| Model       | Key Features                                                                                                                           | Strengths                                                                                                   | Weaknesses                                                                                                 | Suitability                                                  |
| ----------- | -------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------ |
| Waterfall   | - Linear, sequential<br>- Each phase must be completed before the next                                                                 | - Simple, easy to get the hang of<br>- Good for projects with fixed scope<br>- Easy to track progress       | - Rigid, hard to adapt to changes<br>- Very late discovery of bugs<br>- No working software till very late | Small project with fixed, clear requirements                 |
| Incremental | - Develops in small increments<br>- Each increment adds functionality<br>- User feedback after each increment.                         | - Partial product early<br>- Easier testing<br>- Flexible for evolving reqs                                 | - Needs good design from the get go<br>- Integration challenges.                                           | Projects with clear vision, but evolving details             |
| V-Model     | - Waterfall, with corresponding testing/ development phase<br>-High emphasis on validation                                             | - High quality assurance<br>- Early detection of defects<br>- Clear deliverable phases                      | - Extremely rigid<br>- Very expensive to fix changes<br>- Not flexible for iterative feedback              | Safety-critical projects (healthcare, defense)               |
| Iterative   | - Develop in repeated cycles<br>- Each cycle refines the previous<br>- Feedback incorporated with each iterations                      | - Early delivery of working software<br>- Continuous improvement<br>- Flexible to changes.                  | - Scope creep<br>- Requires strong management or version control                                           | Complex systems with learning curves or unclear reqs         |
| Spiral      | - Iterative + Systematic risk analysis<br>- Includes risk assessment, dev, testing                                                     | - High focus on risk management<br>- Flexible and adaptive                                                  | - Complex to manage<br>- High cost and req expertise<br>                                                   | High-risk, high-budget systems (banking)                     |
| Agile       | - Iterative, time-boxed sprints  <br>- Continuous feedback and delivery  <br>- Emphasizes customer collaboration and adaptive planning | - Highly flexible  <br>- Rapid delivery of software <br>- Encourages collaboration and communication        | - Needs active user involvement <br>- Harder to predict effort and cost  <br>- Scope creep                 | Fast-changing environments, start-ups, user-centric projects |
| DevOps      | - Integrates development and IT operations  <br>- Focuses on automation, CI/CD  <br>- Strong monitoring & feedback loops               | - Rapid deployment cycles  <br>- Automation improves efficiency  <br>- Promotes collaboration between teams | - Tooling complexity  <br>- Security and compliance require extra attention                                | Projects require frequent updates(SaaS, cloud)               |
Or in general: 
- **Waterfall / V-Model**: Structured, best for predictable projects.
- **Incremental / Iterative**: Flexibility with manageable releases.
- **Spiral**: Adds risk management for high-stake projects.
- **Agile / DevOps**: Embrace change, fast delivery, modern environments.