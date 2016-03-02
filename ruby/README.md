Ruby
====

Build
-----

Uses [Bundler](http://bundler.io/) to manage dependencies and [rvm](https://rvm.io/) to manage the ruby version.

```bash
mkdir ruby-example
cd ruby-example

rvm --ruby-version use 1.9.3
echo "ruby '1.9.3'\nsource 'https://rubygems.org'\ngem 'rspec'" > Gemfile

gem install bundler
bundle install

mkdir example
cat > example/script.rb <<END
def foo()
  return true
end
END

rspec --init
cat > spec/example_spec.rb <<END
require './example/script.rb'

describe "Example" do
  it "foo()returns true" do
    expect(foo()).to eq(true)
  end
end
END
```

Test
----

```bash
rspec
```

Git
---

```bash
git init
git add .rspec .ruby-version example spec Gemfile Gemfile.lock
git commit -m "Adds sample files"
```
