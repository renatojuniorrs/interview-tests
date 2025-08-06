## 🧭 ZENIT–POLAR Cipher (Python)

The **ZENIT–POLAR cipher** is a classic substitution cipher based on two five-letter words: `ZENIT` and `POLAR`. Each letter in the word `ZENIT` is substituted with the corresponding letter in `POLAR`, and vice versa.

This results in the following **symmetric mapping**:

| Z | E | N | I | T |
| - | - | - | - | - |
| P | O | L | A | R |

This means:

* Z ⇄ P
* E ⇄ O
* N ⇄ L
* I ⇄ A
* T ⇄ R

Applying the cipher **twice** returns the original text. This simple cipher is not suitable for real encryption, but it’s a great exercise.

## 📝 Task

Write a **Python function** that applies the ZENIT–POLAR cipher to a given string.

### ✅ Requirements

1. Replace each letter using the ZENIT–POLAR mapping.
2. Handle **uppercase and lowercase** letters correctly, preserving case.
3. Leave characters that are **not part of the mapping** (spaces, punctuation, digits, etc.) **unchanged**.
4. The function must work for both **encoding and decoding** (i.e., symmetric behavior).


## 📚 Examples

| Input                    | Output                    |
| ------------------------ | ------------------------- |
| `"Zenit"`                | `"Polar"`                 |
| `"Polar"`                | `"Zenit"`                 |
| `"ZENIT POLAR"`          | `"POLAR ZENIT"`           |
| `"International"`        | `"Alrotliraelin"`       |
| `"Zebra in the Zoo"`     | `"Pobti al rho Pee"`      |
| `"Nothing to Translate"` | `"Lerhalg re Rtilsniro"` |


## 🧑‍💻 Function Signature

```python
# Create a new notebook in Google Colab https://colab.research.google.com/
# This must be your first code block
def zenit_polar_cipher(text: str) -> str:
    pass
```

## 🧪 Example Test Cases

You may use the following code to test your solution:

```python
# This can be your second block

def test_zenit_polar_cipher():
    test_cases = [
        ("Zenit", "Polar"),
        ("Polar", "Zenit"),
        ("ZENIT POLAR", "POLAR ZENIT"),
        ("International", "Alrotliraelin"),
        ("Zebra in the Zoo", "Pobti al rho Pee"),
        ("Nothing to Translate", "Lerhalg re Rtilsniro"),
    ]

    for inp, expected in test_cases:
        result = zenit_polar_cipher(inp)
        assert result == expected, f"Failed for '{inp}'. Expected: '{expected}', Got: '{result}'"

    print("All tests passed!")


# test_zenit_polar_cipher()
```
