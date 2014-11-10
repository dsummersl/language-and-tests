Ruby
====

Build
-----

Uses [Bundler](http://bundler.io/) to manage dependencies.

```bash
echo "source 'https://rubygems.org'\ngem 'rspec'" > Gemfile
bundle install
rspec --init
cat > spec/example_spec.rb <<END
describe "Example" do
  it "returns 1" do
    expect(1).to eq(1)
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
git add .rspec spec Gemfile Gemfile.lock
git commit -m "Adds rspec sample tests"
```
