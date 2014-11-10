Python
======

Build
-----

Uses [Nose](https://nose.readthedocs.org) as the test tool.

```bash
mkdir tests

echo "
from nose.tools import *

def test_example():
  ok_(True)
" > tests/example_test.py
```

Test
----

```bash
nosetests
```

Git
---

```bash
echo "*.pyc" > .gitignore
git add tests .gitignore
git commit -m "Adds python example test."
```
