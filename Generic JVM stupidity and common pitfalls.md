### Preface
All questions without any additional info is by default: "Find what's wrong".
### Question 1:
```Java
public class Test1 {
    public static void main(String[] args) {
        int x = 5;
        if (x > 0) {
            int y = 10;
        }
        System.out.println(y);
    }
}

```
### Question 2:
```Java
public class Test2 {
    public static void main(String[] args) {
        String s1 = "Hello";
        String s2 = "Hello";
        if (s1 == s2) {
            System.out.println("Strings are equal");
        }
    }
}

```
### Question 3:
```Java
public class Test3 {
    public static void main(String[] args) {
        int[] arr = {1, 2, 3};
        System.out.println(arr[3]);
    }
}

```
### Question 4:
```Java
public class Test4 {
    public static int square(int x) {
        if (x > 0)
            return x * x;
    }

    public static void main(String[] args) {
        System.out.println(square(5));
    }
}

```
### Question 5:
```Java
public class Test5 {
    public static void main(String[] args) {
        int result = 5 / 2;
        System.out.println(result);
    }
}

```
### Question 6:
```Java
public class Test6 {
    int value;

    public void Test6(int value) {
        this.value = value;
    }

    public static void main(String[] args) {
        Test7 obj = new Test7(10);
        System.out.println(obj.value);
    }
}

```
### Question 7:
```Java
public class Test7 {
    public static void main(String[] args) {
        double a = 0.1;
        double b = 0.2;
        if (a + b == 0.3) {
            System.out.println("Equal");
        }
    }
}

```
### Question 8:
```Java
public class Test8 {
    public static void main(String[] args) {
        final int x = 10;
        x = 20;
        System.out.println(x);
    }
}

```
### Question 9:
```Java
public class Test9 {
    public static void main(String[] args) {
        try {
            System.out.println("Try");
            return;
        } finally {
            System.out.println("Finally");
        }
    }
}

```
What's expected to be printed out here?
### Question 10:
```Java
public class Test10 {
    static int x = 5;

    static {
        x = x + 5;
    }

    static int y = x + 5;

    public static void main(String[] args) {
        System.out.println("y = " + y);
    }
}

```
What's the expected value of `y`?
### Question 11:
```Java
public class Test11 {
    public static void main(String[] args) {
        Integer a = 127;
        Integer b = 127;
        Integer c = 128;
        Integer d = 128;

        System.out.println(a == b);
        System.out.println(c == d);
    }
}

```
What's the expected value of the function?

### Question 12:
```Java
public class Test12 {
    public static void main(String[] args) {
        A obj = new B();
        obj.print();
    }
}

class A {
    public void print() {
        System.out.println("A");
    }
}

class B extends A {
    public void print() {
        System.out.println("B");
    }
}

```
Is there anything wrong with this code? What do you expect it to print?
### Question 13:
```Java
import java.util.*;

public class Test13 {
    public static void main(String[] args) {
        List list = new ArrayList<String>();
        list.add(10);
        String s = (String) list.get(0);
        System.out.println(s);
    }
}

```
### Question 14:
```Java
public class Test14 <T> {
    T[] arr = new T[10];  // Error here?

    public static void main(String[] args) {
        System.out.println("Test");
    }
}

```

### Question 15:
```Java
import java.util.*;

public class Test15 {
    public static void addNumber(List<? super Integer> list) {
        list.add(5);
    }

    public static void main(String[] args) {
        List<Object> list = new ArrayList<>();
        addNumber(list);
        System.out.println(list.get(0).intValue());
    }
}

```
### Question 16:
```Java
public class Test16<T> {
    public static void print(T item) {
        System.out.println(item);
    }

    public static void main(String[] args) {
        Test16.print("Hello");
    }
}

```
### Question 17:
```Java
import java.util.*;

public class Test17 {
    public static void printList(List<?> list) {
        list.add(null);
    }

    public static void main(String[] args) {
        List<String> list = new ArrayList<>();
        printList(list);
        System.out.println(list.size());
    }
}
```
### Question 18:
```Java
public class Test18 {
    public static void main(String[] args) {
        int x = 10;
        Runnable r = () -> {
            System.out.println(x);
        };
        x = 20;
        r.run();
    }
}
```
### Question 19:
```Java
import java.util.*;

public class Test19 {
    public static void main(String[] args) {
        Optional<String> opt = Optional.of("test");
        String result = opt.map(s -> {
            if (s.length() > 3) return s.toUpperCase();
            else return null;
        }).orElse("default");
        System.out.println(result);
    }
}

```
### Question 20:
```Java
import java.util.*;

public class Test20 {
    public static void main(String[] args) {
        List<String> list = Arrays.asList("a", "bb", "ccc");
        list.sort((a, b) -> a.length() - b.length());
        System.out.println(list);
    }
}
```