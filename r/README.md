R
=

This example configuration uses [testthat](http://github.com/hadley/testthat).
Runit is another alternative.

This assumes that `testthat` is already installed. Use
`install.packages("testthat")` to do it from R.

Build
-----

```bash
cat > example.R <<END
return2 <- function () { 2 }
END
cat > test_example.R <<END
library(testthat)

source("example.R")

test_that("return2() returns 2", {
  expect_equal(return2(),2)
})
END
```

Test
----

```bash
echo 'library(testthat) ; test_dir(".")' | R --no-save
```

Git
---

```bash
git add .
git commit -m "Adds R default layout."
```
