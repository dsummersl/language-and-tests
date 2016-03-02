Node JS
=======

Build
-----

Rather than pick a build tool like gulp/grunt, this just uses npm for quick/fast
setup.

Use [nvm](https://github.com/creationix/nvm) to control which version of node
you want to use.

```bash
mkdir node-example
cd node-example

# pick node version
echo 4.2.2 > .nvmrc
nvm use
npm init -f

# setup npm test:
sed -E -i bk 's#"test":.*$#"test": "./node_modules/.bin/mocha tests"#' package.json
npm install --save-dev mocha chai
./node_modules/.bin/mocha init tests

mkdir src
cat > src/example.js <<END
module.exports.exampleFunction = function() {
  return true;
};
END

cat > tests/tests.js <<END
var should = require('chai').should();
var example = require('../src/example');

describe('example', function() {
  it('passes', function() {
    (example.exampleFunction()).should.equal(true);
  });
});
END
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
git add tests src package.json .gitignore .nvmrc
git commit -m "Adds sample files"
```
