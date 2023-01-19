# Introduction to SQL Statements

## Database Design

![design](../resources/design_process.JPG)

<hr>

- **Table**: **A table is a collection of records that sits in our db.**
  - A table generally can be though to hold things of a like kind, in our example case, the table is holding cities.

![table](../resources/table.JPG)

<hr>

- Tables contain **columns**.
  - **Columns represents one property of the type of item that this table is intended to hold.**
  - In our example case *each column represents one property* of a city.
- Each **column must indicate the type** of the data held in it.

![column](../resources/columns.JPG)

- Tables also contain **rows**.
  - **Rows hold a single instance (or record) of the items within the table.**
  - In our example case, *Seattle would be a single instance of a city*, and it's information would be contained in a single row.

![row](../resources/rows.JPG)

<hr>

## Creating Tables

- We will begin by using a browser based tool called: [pg-sql.com](pg-sql.com)

![pgsql.com](../resources/pg-sql-site.JPG)



- **Always double check for correctness before submitting a query!!**

<br>
- Creating a cities table with 4 properties:

![create table](../resources/create_table.jpg)

- This CREATE TABLE will look like this once the call is executed:

![table](../resources/cities.JPG)

<hr>

## Analyzing CREATE TABLE

- **Keywords:** Tell the database that we want to do something. Always written with **UPPERCASE** letters.
  - Can be thought of as instructions.
- **Identifiers:** Tell the database what thing we want to act on. Always written with **lowercase** letters.

![analysis](../resources/analysis.JPG)

![props](../resources/props.JPG)

![data](../resources/column_data.JPG)

- **VARCHAR** can be thought of as a string.
- It is important to understand the bounds of the data types.

<hr>

## Inserting Data Into a Table

- Query:
  - Keywords: INSERT INTO 
  - Identifier: cities
  - Columns within parenthesis

![insert](../resources/insert.JPG)

- What is important is that we match the data we want to insert in the same order as the column we wish to insert the data into:

![insert diagram](../resources/insert_diagram.JPG)

- We can insert multiple rows with one insert statement by adding row values separated by commas:

![multi](../resources/insert_multi.JPG)

<hr>

## Retrieve Data with Select

- To pull all the information from a table we can use the `*` character with the SELECT and FROM keywords:

![all](../resources/select_all.JPG)

- To pull all values from specific columns you can use the column(property) name:

![some](../resources/select_some.JPG)


<hr>

## Calculated Columns

- SQL is not just about pulling raw data out of a table.
- **We can write SQL to *transform* or *process* our data before we receive it.**

For Example, we can calculate the population density by dividing the population by the area.
- **Notice:** The newly created column has a name of `?column?`. SQL knows we have done some math, but it doesn't know what to call it.

![calc](../resources/calc_noName.JPG)

- We can add a name using the AS keyword.
- **Notice:** Now the new column has the name `density`.

![calc_name](../resources/calculate.JPG)

- Example of some of the math operations we can do on the data.

![math](../resources/operators.JPG)

<hr>

## String Operators and Functions

- We can use operators and functions to manipulate strings:

![strings](../resources/strings.JPG)

- Operator Example:

![concat](../resources/concat.JPG)

- Function Example:

![concat](../resources/concat1.JPG)

- Example of nested function calls:
  - **Notice:** the upper function call within the CONCAT function call.

![upper](../resources/upper.JPG)