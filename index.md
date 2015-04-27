---
layout: default
title: Welcome
---

# {{ page.title }}

<div class="toc" markdown="1">
Contents:

* [What's `world.db`?](#whatis)
* [Datasets](#datasets)
    * [Countries](#countries)
    * [Cities](#cities)
* [Web Admin Site](#webadmin)
* [About, License](#license)
* [Questions? Comments?](#questions)
</div>



## What's `world.db`?   {#whatis}

A free open public domain world database 'n' schema
for use in any (programming) language (e.g. uses plain text datasets).

**Schema Diagram**

![](i/worlddb-models.png)

Everything is a place.

![](i/worlddb-models-place.png)


## Datasets  {#datasets}

### Countries  {#countries}

~~~
ca, Canada,          CAN, 9 984 670 km²,  34 278 406, un|north america
mx, México [Mexico], MEX, 1 972 550 km², 112 322 757, un|north america
us, United States,   USA, 9 629 091 km², 314 167 157, un|north america
~~~

Source: [`north-america/countries.txt`](https://github.com/openmundi/world.db/blob/master/north-america/countries.txt):

### Cities  {#cities}

~~~
Toronto,            ON,   5 583 064
Montréal|Montreal,  QC,   3 824 221
Vancouver,          BC,   2 313 328
Ottawa,             ON,   1 236 324
Calgary,            AB,   1 214 839
Edmonton,           AB,   1 159 869
Québec,             QC,     765 706
Winnipeg,           MB,     730 018
~~~

Source: [`north-america/ca-canada/cities.txt`](https://github.com/openmundi/world.db/blob/master/north-america/ca-canada/cities.txt):


## Web Admin Site   {#webadmin}

Try the `world.db` web admin app running
on Heroku [`worlddb.herokuapp.com`](http://worlddb.herokuapp.com).


## Real World Usage

[world.db.admin](https://github.com/geraldb/world.db.admin) - A free, open source web admin tool for world.db in Ruby on Rails (version 3.2 and up).

[sport.db](https://github.com/opensport) - free open public domain sports database & schema.

[football.db](https://github.com/openfootball) -  free open public domain football (soccer) database & schema

[formula1.db](https://github.com/opensport/formula1.db) - free open public domain Formula 1/Formula One database & schema

[ski.db](https://github.com/opensport/ski.db) -  free open public domain ski alpin/alpine ski database & schema

[beer.db](https://github.com/openbeer) - free open public domain beer database & schema

[Sportbook](https://github.com/openbookie/sportbook) - free, open source sports betting (prediction) pool
in Ruby on Rails (version 3.2 and up). 


## Alternatives

See the [`awesome-world`](https://github.com/planetopendata/awesome-world) page at the Planet Open Data.


## License    {#license}

The `world.db` schema, data and scripts are dedicated to the public domain.
Use it as you please with no restrictions whatsoever.


{% include questions.md %}

