## 🧠 Code Smell & Bug Fixing Challenge (Java)

### Objective

Evaluate the candidate’s ability to **detect**, **analyze**, and **fix subtle bugs** in existing code — and to **explain how they’d help a teammate** who wrote it.


### Description

You are reviewing a junior developer’s code.
They’ve implemented a function to calculate the **average score** from a list of integers.

However, the code seems *almost correct* — but it occasionally returns wrong results or even crashes.

Your job is to:

1. Identify **bugs or potential issues** in the code.
2. Suggest **improvements** (code + reasoning).
3. Describe how you would **help the teammate** understand and fix it without discouraging them.


### Provided Code

```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        testAverageScore();
    }

    // Returns the average score of a list of integers
    public static double averageScore(List<Integer> scores) {
        int total = 0;
        for (int i = 0; i <= scores.size(); i++) {
            total += scores.get(i);
        }
        return total / scores.size();
    }

    // Test function
    public static void testAverageScore() {
        List<Integer> scores1 = Arrays.asList(10, 20, 30);
        System.out.println("Expected 20.0, got: " + averageScore(scores1));

        List<Integer> scores2 = new ArrayList<>();
        System.out.println("Expected 0.0, got: " + averageScore(scores2));

        List<Integer> scores3 = Arrays.asList(1, 2, 2);
        System.out.println("Expected 1.67, got: " + averageScore(scores3));
    }
}
```

### Tasks

1. **Find and explain at least 3 issues** (logical, runtime, or best-practice related).


### Recommended Test Environment

👉 [https://www.onlinegdb.com/online_java_compiler](https://www.onlinegdb.com/online_java_compiler)


### Expected Output (after fixing)

```
Expected 20.0, got: 20.0
Expected 0.0, got: 0.0
Expected 1.67, got: 1.67
```

