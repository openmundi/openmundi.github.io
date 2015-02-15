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
Wien [Vienna], W,   1 731 236
Graz,          ST,    265 318
Linz,          O,     191 107
Salzburg,      S,     148 521
Innsbruck,     T,     121 329
~~~

Source: [`europe/at-austria/cities.txt`](https://github.com/openmundi/world.db/blob/master/europe/at-austria/cities.txt):


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

[geonames.org](http://geonames.org) - open geo (geographical) database covers all countries and contains over eight million placenames

[worlddb](http://code.google.com/p/worlddb) -  open world database alpha; includes country, region & city names in many languages names and latitude and longitude numbers and country's iso 2-letter code.

[countries](https://github.com/hexorx/countries) - world countries; includes data from ISO 3166 (countries and states/subdivisions ), ISO 4217 (currency), and E.164 (phone numbers).

[countries](https://github.com/mledoze/countries) - world countries with iso codes, currencies and more in JSON, CSV and XML.

[django-cities](https://github.com/coderholic/django-cities) - python script for importing countries, regions, cities etc. from geonames.org

[current-countries-of-earth](https://github.com/ewheeler/current-countries-of-earth) - python script to fetch current ISO 3166 country info; output as JSON



## License    {#license}

The `world.db` schema, data and scripts are dedicated to the public domain.
Use it as you please with no restrictions whatsoever.


{% include questions.md %}

