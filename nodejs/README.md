Node JS
=======

Build
-----

To skip all the details one would normally have to enter, use `npm init -f`.

Rather than pick a build tool like gulp/grunt, this just uses npm for qiuck/fast
setup.

```bash
mkdir nodejs
cd nodejs
npm init -f

# setup npm test:
sed -E -i bk 's#"test":.*$#"test": "./node_modules/.bin/mocha tests"#' package.json
npm install --save-dev mocha chai
./node_modules/.bin/mocha init tests

echo "
var should=require('chai').should();

describe('example', function() {
  it('passes', function() {
    (true).should.equal(true);
  });
});" > tests/tests.js
```

Test
----

```bash
npm test
```

Git
---

```bash
git init
echo "node_modules" > .gitignore
git add README.md tests package.json .gitignore
git commit -m "Sets up mocha testing"
```
