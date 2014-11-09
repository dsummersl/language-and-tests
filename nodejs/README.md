Node JS
=======

To skip all the details one would normally have to enter, use `npm init -f`.

```bash
mkdir nodejs
cd nodejs
npm init -f
```

Rather than pick a build tool like gulp/grunt, this just uses npm.

Mocha & Chai
------------

```bash
# setup npm test:
sed -E -i bk 's#"test":.*$#"test": "./node_modules/.bin/mocha tests"#' package.json
npm install --save-dev mocha chai
./node_modules/.bin/mocha init tests
```

At this point you can run tests:

```bash
npm test
```

Add a sample test:

```bash
echo "
var should=require('chai').should();

describe('example', function() {
  it('passes', function() {
    (true).should.equal(true);
  });
});" > tests/tests.js
```