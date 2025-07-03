## Bug in Reversed Family Member List

### 📝 Problem Statement

You are given a Go program that models a simple family tree. The `Server` struct holds a list of `FamilyMember`s and a `map[string][]string` representing parent-child relationships.

Your task is to:

1. **Identify the bug** in `getReversedFamilyBuggy`.
2. **Explain why it happens.**
3. **Fix the bug** in a separate function.

You can use https://go.dev/play/ to test this code.

---

### 📄 Provided Code

```go
package main

import (
	"fmt"
)

// FamilyMember represents a member in the family tree
type FamilyMember struct {
	ID   int
	Name string
}

type Server struct {
	Members []*FamilyMember
	Tree    map[string][]string
}

func (s *Server) loadMembers() {
	names := []string{"John", "Anna", "Mike", "Sarah"}
	for i, name := range names {
		m := &FamilyMember{ID: i + 1, Name: name}
		s.Members = append(s.Members, m)
	}
}

func (s *Server) loadFamilyTree() {
	s.Tree = map[string][]string{
		"John":  {"Anna", "Mike"},
		"Anna":  {"Sarah"},
		"Mike":  {},
		"Sarah": {},
	}
}

func reverse(s string) string {
	r := []rune(s)
	for i, j := 0, len(r)-1; i < j; i, j = i+1, j-1 {
		r[i], r[j] = r[j], r[i]
	}
	return string(r)
}

func (s *Server) getReversedFamilyBuggy() []*FamilyMember {
	var reversed []*FamilyMember
	var temp FamilyMember

	for _, member := range s.Members {
		temp.ID = member.ID
		temp.Name = reverse(member.Name)
		reversed = append(reversed, &temp)
	}

	return reversed
}


func main() {
	srv := &Server{}
	srv.loadMembers()
	srv.loadFamilyTree()

	fmt.Println("=== BUGGY reversed family members ===")
	buggy := srv.getReversedFamilyBuggy()
	for _, m := range buggy {
		fmt.Printf("ID: %d, Name: %s\n", m.ID, m.Name)
	}

}
```
