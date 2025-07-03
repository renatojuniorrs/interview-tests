## ✅ Validate ABCD Bank Credit Card Numbers

(Test Source: https://www.hackerrank.com/)

Fredrick recently received `N` credit cards from **ABCD Bank**. He needs to verify if each credit card number is **valid** or **invalid** based on the bank’s rules. Being an expert with regular expressions, you’re here to help!

---

### 📜 Valid Credit Card Rules

A credit card from ABCD Bank is considered **valid** if:

1. It **starts with a 4, 5, or 6**.
2. It **contains exactly 16 digits**.
3. It **only contains digits (0-9)**.
4. It **may** have digits in groups of 4, separated by a single hyphen `-`.
5. It **must not use any other separator** (such as space `' '`, underscore `'_'`, etc.).
6. It **must not have 4 or more consecutive repeated digits** (like `4444`).

---

### ✅ Valid Examples

```
4253625879615786
4424424424442444
5122-2368-7954-3214
```

---

### ❌ Invalid Examples

```
42536258796157867       # 17 digits → Invalid
4424444424442444        # 4 or more consecutive repeated digits → Invalid
5122-2368-7954 - 3214   # Contains space as separator → Invalid
44244x4424442444        # Contains non-digit character 'x' → Invalid
0525362587961578        # Doesn't start with 4, 5, or 6 → Invalid
```

---

### 📥 Input Format

```
First line: An integer N (number of credit card numbers)
Next N lines: Each line contains a credit card number as a string
```

---

### 📤 Output Format

For each credit card number, output:

```
Valid     → if the number meets all conditions
Invalid   → otherwise
```

---

### 🔒 Constraints

* `1 <= N <= 100`
* Each card number is a string

---

### 🧪 Sample Input

```
6
4123456789123456
5123-4567-8912-3456
61234-567-8912-3456
4123356789123456
5133-3367-8912-3456
5123 - 3567 - 8912 - 3456
```

---

### ✅ Sample Output

```
Valid
Valid
Invalid
Valid
Invalid
Invalid
```

---

### 💡 Explanation

* `4123456789123456` → Meets all rules.
* `5123-4567-8912-3456` → Proper format and valid.
* `61234-567-8912-3456` → Grouping is not consistent → Invalid.
* `4123356789123456` → Valid.
* `5133-3367-8912-3456` → Repeats `3333` → Invalid.
* `5123 - 3567 - 8912 - 3456` → Uses spaces → Invalid.


### 1. **Project Setup**

Assume you have two files in a directory called `tests`:

```
~/go/tests/
├── main.go          // your Go implementation
└── main_test.go     // your test cases
```

### 2. **Initialize a Go Module (only once per project)**

From inside the `tests` folder:

```bash
cd ~/go/tests
go mod init coding-test.com/tests
```

This creates a `go.mod` file which Go uses to manage dependencies.

---

### 3. **Write Your Test File**

Ensure `main_test.go` looks like this:

```go
package main

import "testing"

func TestIsValidCreditCard(t *testing.T) {
	tests := []struct {
		cardNumber string
		expected   bool
	}{
		{"4123456789123456", true},
		{"5123-4567-8912-3456", true},
		{"4123356789123456", true},
		{"61234-567-8912-3456", false},
		{"5133-3367-8912-3456", false},
		{"5123 - 3567 - 8912 - 3456", false},
		{"42536258796157867", false},
		{"4424444424442444", false},
		{"44244x4424442444", false},
		{"0525362587961578", false},
	}

	for _, test := range tests {
		result := isValidCreditCard(test.cardNumber)
		if result != test.expected {
			t.Errorf("Failed for %q: expected %v, got %v", test.cardNumber, test.expected, result)
		}
	}
}
```

---

### 4. **Run the Tests**

From inside the project directory (`~/go/tests`):

```bash
go test
```

This runs all tests in `*_test.go` files and shows a pass/fail result for each.

