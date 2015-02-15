
* [Tables, Schema](#schema)

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
