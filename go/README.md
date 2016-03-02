Go
==

Build
-----

```bash
mkdir go-example
cd go-example

cat > example.go <<END
package example

func exampleFunction() error {
  return nil
}
END

cat > example_test.go <<END
package example

import "testing"

func TestExample(t *testing.T) {
  if exampleFunction() != nil {
    t.Errorf("It didn't work!")
  }
}
END
```

Test
----

```bash
go test
```

Git
---

```bash
git init
git add .
git commit -m "Adds sample files"
```
