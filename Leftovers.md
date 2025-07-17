
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

Type Conversion in Java is like buil]ding a house. You building more of the house is free and is done automatically, you break down the house requires explicit permissions. Generally speaking, remember this list, going from smallest to biggest:

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