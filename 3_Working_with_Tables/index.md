# Working with Tables

## The Plan Moving Forwards

- Most all dbs have more than one table.
- Moving forward we will be working on a db for a photo sharing app.

<hr>

## Approach to Database Design

![photo](../resources/photodb.JPG)

### What tables should we make?

- Whatever type of db you are making, it will most likely hold features that are common to many applications, eg: authentication, comments etc...
  - **There are tons of resources online on how to structure and implement your database for these features.**
  - GOOGLE IS YOUR FRIEND
- Identify/define what resources your application will need.
- Build mock ups for your application ahead of time.
- Find *relationships* or *ownerships* between tables in your db.

![instagram](../resources/insta.JPG)

## One-to-Many and Many-to-One Relationships

### The four relationships:

1. One-to-Many
  - User to Photos
  - From the **perspective** of the user.
  - There can be many photos, but they can only belong to one user.

![one to many](../resources/one-to-many.JPG)

2. Many-to-One
  - There can be many photos, but they can only belong to one user.
  - From the **perspective** of the photos.

![otm](../resources/otm-mto.JPG)