Groovy
======

Build
-----

Uses [GvmTool](http://gvmtool.net) to setup gradle.

```bash
mkdir groovy-example
cd groovy-example

sdk use gradle 2.11
sdk use groovy 2.4.6

gradle init --type=groovy-library
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
