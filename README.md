# Personal Library

## Instructions

### Phase 1 - Database setup/configuration using Sequelize
  - Connect to our mysql database using the sequelize npm package
  - Use the sequelize CLI to create our config and models folder
  - Edit the config.json to our database credentials and database name

### Phase 2 - Models
  - Authors
    - firstName
    - lastName
    - Association - create a hasMany relationship between Authors and Books

  - Books
    - title
    - coverPhoto
    - authorId (foreign key column)
    - Association(s): 
      - create a belongsTo relationship between Books and Authors
      - create a hasMany relationship between Books and Notes

  - Notes
    - note
    - bookId (foreign key column)
    - Association:
      - create a belongsTo relationship between Notes and Books

### Phase 3 - Controllers
  Author Controller

    - GET Route
      - Author.findAll Authors: include a join on Books
      - POST Route
        - Author.create: adding a Author
    - TEST these routes and create authors via POSTMAN

  Book Controller

    - GET Route
      - Book.findAll Books: include a join on Authors
    - POST Route
      - Book.create: adding a Book
    - GET Route
      - Book.findAll: include a join on Notes
  
  Notes Controller
  
    - GET Route
      - Note.findAll: include a join on Books
    - POST Route
      - Note.create: adding a note to a book
    - DELETE Route
      - Note.destroy: deletes a note