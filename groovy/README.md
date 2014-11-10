Groovy
======

Build
-----

Uses [GvmTool](http://gvmtool.net) to configure/setup gradle.

```bash
gvm use gradle 2.1
gvm use groovy 2.3.7

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
git add .
git commit -m "Adds gradle's groovy library template."
```
