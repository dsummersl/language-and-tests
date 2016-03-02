R
=

This assumes that `testthat` is already installed. Use
`install.packages("testthat")` to do it from R.

Build
-----

```bash
mkdir r-example
cd r-example

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

This configuration uses [testthat](http://github.com/hadley/testthat).
Runit is another alternative.

```bash
echo 'library(testthat) ; test_dir(".")' | R -q --no-save
```

Git
---

```bash
git init
git add .
git commit -m "Adds sample files"
```
