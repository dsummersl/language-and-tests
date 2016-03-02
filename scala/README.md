Scala
=====

Build
-----

Uses [GvmTool](http://gvmtool.net) to configure/setup gradle.

```bash
mkdir scala-example
cd scala-example

sdk use gradle 2.1

gradle init --type=scala-library
```

Test
----

```bash
gradle test
```

Git
---

```bash
git init
echo .gradle > .gitignore
echo build >> .gitignore
git add gradle* src build.gradle settings.gradle .gitignore
git commit -m "Adds sample files"
```

