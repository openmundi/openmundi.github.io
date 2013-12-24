---
layout: default
title: How To Build Your Own Copy
---

# {{ page.title }}

<div class="toc" markdown="1">
Contents:

* [Build Your Own `world.db` Copy?](#build)
* [Questions? Comments?](#questions)
</div>


## Build Your Own `world.db` Copy?   {#build}


Use the `worlddb` command line tool to build yourself a copy of
the `world.db` from the plain text fixtures in two steps.

Step 1:  Get a copy of the `world.db` fixtures

    $ git clone git://github.com/openmundi/world.db.git

Step 2:  Let's build the `world.db`

    $ worldb setup --include ./world.db

That's it. See the [`worlddb` command line tool project](https://github.com/geraldb/world.db.ruby)
for more.


![](https://raw.github.com/openmundi/openmundi.github.io/master/i/sqlitestudio.png)



{% include questions.md %}


