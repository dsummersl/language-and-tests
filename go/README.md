Go
==

```bash
cat > example_test.go <<END
package example

import "testing"

func TestExample(t *testing.T) {
  if false {
    t.Errorf("It didn't work!")
  }
}
END
```

To run the tests:

```bash
go test
```

Add to Git:

```bash
git init
git add example_test.go
git commit -m "Adds sample test"
```
