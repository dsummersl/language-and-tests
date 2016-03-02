Scala
=====

Build
-----

Uses [GvmTool](http://gvmtool.net) to configure/setup gradle.

```bash
mkdir java-example
cd java-example

sdk use gradle 2.11

gradle init --type=java-library
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

