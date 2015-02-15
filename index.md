---
layout: default
title: Welcome
---

# {{ page.title }}

<div class="toc" markdown="1">
Contents:

* [What's `world.db`?](#whatis)
* [Web Admin Site](#webadmin)
* [Data Sets](#data-sets)
    * [Countries](#countries)
    * [Cities](#cities)
* [Tables, Schema](#schema)
* [About, License](#license)
* [Questions? Comments?](#questions)
</div>



## What's `world.db`?   {#whatis}

A free open public domain world database 'n' schema
for use in any (programming) language (e.g. uses plain text datasets).

**Schema Diagram**

Everything is a place.

![](i/worlddb-models-place.png)

Continents > Countries > States > Cities.

![](i/worlddb-models.png)


**Datasets Examples**

~~~
### Countries

ca, Canada,          CAN, 9_984_670 km²,  34_278_406, un|north america
mx, México [Mexico], MEX, 1_972_550 km², 112_322_757, un|north america
us, United States,   USA, 9_629_091 km², 314_167_157, un|north america
...
~~~

~~~
### Cities

Wien [Vienna], W,  1_731_236, m:1_724_000
Graz,          ST,   265_318
Linz,          O,    191_107
Salzburg,      S,    148_521
Innsbruck,     T,    121_329
...
~~~


## Web Admin Site   {#webadmin}

Try the `world.db` web admin app running
on Heroku [`worlddb.herokuapp.com`](http://worlddb.herokuapp.com).


## Data Sets  {#data-sets}

### Countries  {#countries}

~~~
ca, Canada,          CAN, 9_984_670 km²,  34_278_406, un|north america
mx, México [Mexico], MEX, 1_972_550 km², 112_322_757, un|north america
us, United States,   USA, 9_629_091 km², 314_167_157, un|north america
~~~

Source: [`north-america/countries.txt`](https://github.com/openmundi/world.db/blob/master/north-america/countries.txt):

### Cities  {#cities}

~~~
Wien [Vienna], W,  1_731_236, m:1_724_000
Graz,          ST,   265_318
Linz,          O,    191_107
Salzburg,      S,    148_521
Innsbruck,     T,    121_329
~~~

Source: [`europe/at-austria/cities.txt`](https://github.com/openmundi/world.db/blob/master/europe/at-austria/cities.txt):



The plain text format reader skips comments (starting with `#`)
and blank lines. Example:

~~~
###################################################
# Your comments here
#
~~~

## Tables, Schema   {#schema}

The `world.db` includes the following tables:

* countries
* regions
* cities
* tags
* taggings (many-to-many join table for tags+countries/regions/cities)
* langs
* usages (many-to-many join table for langs+countries)
* props

[add schema pic here]

###  `countries` Table

    CREATE TABLE "countries" (
      "id" INTEGER PRIMARY KEY AUTOINCREMENT NOT NULL,
      "title" varchar(255) NOT NULL,
      "key" varchar(255) NOT NULL,
      "tag" varchar(255) NOT NULL,
      "synonyms" varchar(255),
      "pop" integer,
      "area" integer,
      "created_at" datetime NOT NULL,
      "updated_at" datetime NOT NULL
    );

###  `regions` Table

    CREATE TABLE "regions" (
      "id" INTEGER PRIMARY KEY AUTOINCREMENT NOT NULL,
      "title" varchar(255) NOT NULL,
      "key" varchar(255) NOT NULL,
      "synonyms" varchar(255),
      "country_id" integer NOT NULL,
      "pop" integer, "area" integer,
      "created_at" datetime NOT NULL,
      "updated_at" datetime NOT NULL
    );

###  `cities` Table

    CREATE TABLE "cities" (
      "id" INTEGER PRIMARY KEY AUTOINCREMENT NOT NULL,
      "title" varchar(255) NOT NULL,
      "key" varchar(255) NOT NULL,
      "synonyms" varchar(255),
      "country_id" integer NOT NULL,
      "region_id" integer,
      "pop" integer,
      "area" integer,
      "created_at" datetime NOT NULL,
      "updated_at" datetime NOT NULL
    );


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



## Thank You - Contributors - ¡Gracias! - Obrigado - Danke

Ernesto Chapon - William de Melo Gueiros

## License    {#license}

The `world.db` schema, data and scripts are dedicated to the public domain.
Use it as you please with no restrictions whatsoever.


{% include questions.md %}





