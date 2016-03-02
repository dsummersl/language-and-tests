Python
======

Build
-----

Uses [virtualenv](https://virtualenv.readthedocs.org/en/latest/) and
[pip](https://pip.pypa.io/en/stable/) for package management.

Virtualenv updates your shell to add packages in the `virtualenv` directory to
your path. When you're done, use the `deactivate` command to remove it.

```bash
mkdir python-example
cd python-example

# setup a directory for dependencies and pick the version of python:
virtualenv -p python virtualenv
source virtualenv/bin/activate

echo nose > requirements.txt
pip install -r requirements.txt

mkdir example
touch example/__init__.py
cat > example/script.py <<END
def foo():
  return True
END

mkdir tests
cat > tests/example_test.py <<END
from nose.tools import *
from example.script import *

def test_example():
  ok_(foo())
END
```

Test
----

Uses [Nose](https://nose.readthedocs.org) as the test tool.

```bash
nosetests
```

Git
---

```bash
git init
echo "*.pyc" > .gitignore
echo virtualenv >> .gitignore
git add example tests requirements.txt .gitignore
git commit -m "Adds sample files"
```
