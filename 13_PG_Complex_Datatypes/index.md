# PostgreSQL Complex Datatypes

<hr>
<br>

## PGAdmin and Postgres Server

- PGAdmin - Tool to manage and inspect a Postgres database. - Can connect to local or remote databases (e.g. AWS). - Can view/change just about anything in PG.
  <br>

- Postgres Server
  - When we download pg we are running a pg server locally.
  - A pg server can contain multiple databases.
  - All data for a single application lives on a single db.
  - Having multiple DBs is more about working with more than one app on your machine.

![pg server](../resources/pg_server.JPG)
<br>

## Data Types

![data types](../resources/data_types.JPG)

- These are **CATEGORIES**.
  - They contain subtypes that we can make use of.
- Most important:
  - **Numbers**
  - **Date/Time**
  - **Character**
  - **Boolean**
    <br>

## Numeric Types

![num types](../resources/num_types.JPG)
<br>

## Rules on Numeric Data Types

![num rules](../resources/num_rules.JPG)

- **TYPECASTING:**

  - We can get pg to typecast a value by adding `::<datatype>` after the value we wish to cast.
    ![casting](../resources/casting.JPG)
    <br>

- FLOATING POINT MATH:
  - **The decimal value is often inaccurate in:**
    - real
    - double precision
    - float
    - **But, much more efficient to run.**
  - Less efficient but 100% accurate: - decimal - numeric - Essentially the same.
    <br>

## Character Types:

- **There is NO performance difference between the different char types. So pick whatever one fits your needs.**
  - The char length in CHAR(#) and VARCHAR(#) is just to impose a limit.

![char types](../resources/char_types.JPG)
<br>

## Boolean Data Types

- Some of these values are strings to begin with:

![bool_types](../resources/bool_types.JPG)
<br>

## Dates

- You can provide a string of just about any type and pg is going to format it for you.
  - it will format it to YYYY-MM-DD

![date](../resources/date.JPG)
<br>

## Time (with and without Time Zone)

- Time:
  - You can provide a time and pg will format it to 24h time.
  - Type **TIME** is an alias for "Time without Time Zone"
    - You can put **TIME** or **TIME WITHOUT TIME ZONE**, they will do the same thing.

    ![time](../resources/time_no_TZ.JPG)

- Time with Time Zone:
  - If a time is provided with a time zone, it will be converted into the 24h UTC time value.
  - Type: **TIME WITH TIME ZONE**

    ![time with TZ](../resources/Time_with_TZ.JPG)

- TimeStamp:
  - Given a date and time string of any standard format, pg will format it to be a timestamp value.
  - Type: **TIME STAMP WITH TIME ZONE**
   
    ![timestamp](../resources/timestamp.JPG)
<br>

## Intervals

![intervals](../resources/intervals.JPG)

![interval 2](../resources/interval_2.JPG)
<br>

- **We can do numeric operations on intervals.**
  ![interval math](../resources/interval_math.JPG)
<br>

- **We can also do interval math between timestamps and timestamps, and timestamps and intervals.**
  ![interval TZ math](../resources/interval_tz_math.JPG)
  ![tz math](../resources/tz_math.JPG)
<br>

[<< PREV](../13_PG_Complex_Datatypes/index.md) - [HOME](../Frontpage/index.md) - [NEXT >>](../14_DB_side_Validation/index.md)
