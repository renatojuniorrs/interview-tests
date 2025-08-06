## 🧭 ZENIT–POLAR Cipher

The **ZENIT–POLAR cipher** is a classic substitution puzzle often used in beginner cryptography and programming challenges.

It originates from Latin America, commonly appearing in logic magazines and classrooms. It uses **two five-letter words**, **ZENIT** and **POLAR**, as a key to perform letter substitutions. Each letter in `ZENIT` is substituted with the corresponding letter in `POLAR`, and vice versa.

The pairs are:

| Z | E | N | I | T |
| - | - | - | - | - |
| P | O | L | A | R |

This gives us a **symmetric mapping**, meaning applying the cipher twice returns the original text. The cipher is not secure for real-world use, but it’s excellent for practicing coding skills.

---

## 📝 Task

Implement a Go function that performs the **ZENIT–POLAR cipher** transformation on a string. Your function should:

### ✅ Requirements:

1. Replace each letter according to the ZENIT–POLAR mapping.
2. Handle **both upper and lowercase letters**, preserving the **original case**.
3. Leave non-mapped characters (spaces, punctuation, digits) **unchanged**.
4. The function should work for **both encoding and decoding**.

---

## 📚 Examples

| Input                    | Output                    |
| ------------------------ | ------------------------- |
| `"Zenit"`                | `"Polar"`                 |
| `"Polar"`                | `"Zenit"`                 |
| `"ZENIT POLAR"`          | `"POLAR ZENIT"`           |
| `"International"`        | `"Alrotliraelin"`       |
| `"Zebra in the Zoo"`     | `"Pobti al rho Pee"`      |
| `"Nothing to Translate"` | `"Lerhalg re Rtilsniro"` |

---

## 🔧 Starter Code (Go)

```go
package main

import (
	"fmt"
	"strings"
	"unicode"
)


func zenitPolarCipher(text string) string {
	
	return 
}

func main() {
	fmt.Println(zenitPolarCipher("Zenit and Polar")) // Should print: Polar lnd Zenit
}
```

---

## 🧪 Optional Test File

If you want to verify your solution automatically, use this simple Go test:

```go
// zenitpolar_test.go
package main

import "testing"

func TestZenitPolarCipher(t *testing.T) {
	tests := []struct {
		input    string
		expected string
	}{
        {"Zenit", "Polar"},
        {"Polar", "Zenit"},
        {"ZENIT POLAR", "POLAR ZENIT"},
        {"International", "Alrotliraelin"},
        {"Zebra in the Zoo", "Pobti al rho Pee"},
        {"Nothing to Translate", "Lerhalg re Rtilsniro"},
	}

	for _, tt := range tests {
		output := zenitPolarCipher(tt.input)
		if output != tt.expected {
			t.Errorf("For input '%s', expected '%s', got '%s'", tt.input, tt.expected, output)
		}
	}
}
```
