# Relating Records with Joins

- In this section we are going to be working with a prebuilt db for a basic photo sharing app:

![photos db](../resources/photos-db.JPG)

<hr>
<br>


## Queries with Joins and Aggregators

![joins and aggregators](../resources/j_and_a.JPG)

## Joining Different Tables

- Here we are going to try to display the content of the comment along with the username of the commenter.
  - Note that the username and the comment are in different tables.

![pg join](../resources/pg-join.jpg)

- When we ask pg to `JOIN` tables we can think of it as temporarily creating a new table matching rows as the condition defines.

![user comment](../resources/user_comment.JPG)

- One more example query using `JOIN` to display comments and the url for the associated photo:

![photo](../resources/photo_join.JPG)

## Alternate Forms of Syntax

- Table order between `FROM` and `JOIN` will *usually* many a difference.
<br>
- We must give context if column names collide.
  - If this happens we will end up with an error statement:
    - `column reference "id" is ambiguous`
  - We can clarify which column we want by adding the table name and a `.` before the column name:
![collide](../resources/collide.JPG)

<br>

- Tables can be renamed using the `AS` keyword.
  - This is convenient when making large or complex queries.
![AS](../resources/AS.JPG)
  - You can also drop the `AS` keyword all together:
    - It is recommended to keep the `AS` for clariety
![No AS](../resources/AS_no.JPG)

<br>

- There are several kinds of 'joins'.

## Missing Data in JOINS & Why Wasn't It Included

- What happens if we want to show every photo in our db and the associated user id, but not all photos have users associated with them (null in 'user_id' field)?
  - If we try something like this:
![null join](../resources/null_join.JPG)
  - We no photos with a `null` value in the user_id field will be shown.

<br>

- It does not join because a `null` value does not meet the `ON` condition.

## Four Kinds of JOINS