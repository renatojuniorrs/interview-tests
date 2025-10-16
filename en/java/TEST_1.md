## Fibonacci Function (Java)

### Objective

Implement and test a function that returns the n-th number in the Fibonacci sequence.

### Description

You need to complete the function `fibonacci(int n)` to return the correct Fibonacci number and create a function `testFibonacci()` to validate its behavior with different test cases.

The Fibonacci sequence starts like this:

```
0, 1, 1, 2, 3, 5, 8, 13, 21, 34, ...
```

That is:

* `fibonacci(0)` → 0
* `fibonacci(1)` → 1
* `fibonacci(2)` → 1
* `fibonacci(3)` → 2
* and so on.

---

### Test Environment

It is recommended to use the online compiler at:
👉 [https://www.onlinegdb.com/online_java_compiler](https://www.onlinegdb.com/online_java_compiler)

---

### Recommended Test Cases

| Input `n` | Expected Output |
| --------- | --------------- |
| 0         | 0               |
| 1         | 1               |
| 2         | 1               |
| 3         | 2               |
| 4         | 3               |
| 5         | 5               |
| 6         | 8               |
| 7         | 13              |
| 10        | 55              |

---

### Starter Code (Boilerplate)

Copy and paste the code below into the Java editor on [OnlineGDB](https://www.onlinegdb.com/online_java_compiler) and complete the `fibonacci` function and the test function:

```java
public class Main {
    public static void main(String[] args) {
        testFibonacci();
    }

    // Function that returns the n-th Fibonacci number (to be completed)
    public static int fibonacci(int n) {
        // TODO: Implement iterative Fibonacci sequence logic
        return -1; // placeholder value
    }

    // Test function
    public static void testFibonacci() {

    }
}
```

---

### ✅ Acceptance Criteria

* The function `fibonacci(int n)` must be **iterative**, not recursive.
* All tests should pass with the correct outputs.
* The code must compile and run without errors on OnlineGDB.
