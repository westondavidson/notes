# what we'll be doing today
- today we'll be doing unit testing in our database
- crud operations for our TOH app

- we want to test our data access to ensure that it works against different connection strings etc.
- debugging our crud operations!
- if you know your data layer works properly you can avoid later on confusion.
- when you unit test against a database, you don't want to test against your real database with real data
- if something goes wrong with the implementation it doesn't affect the existing data.