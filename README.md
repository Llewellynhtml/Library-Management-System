To start your mongo shell type the following command :

mongosh

To create LibraryDB database use the following command :

use LibraryDB

To Create Collections and Insert multiple Documents using insertMany use the following command :

db.BooksCollection.insertMany([ { _id: 1, title: "1984", author_id: 1, genres: ["Dystopian", "Political Fiction"], published_year: 1949, available: true }, { _id: 2, title: "To Kill a Mockingbird", author_id: 2, genres: ["Southern Gothic", "Bildungsroman"], published_year: 1960, available: true }, { _id: 3, title: "The Great Gatsby", author_id: 3, genres: ["Tragedy"], published_year: 1925, available: true }, { _id: 4, title: "Brave New World", author_id: 4, genres: ["Dystopian", "Science Fiction"], published_year: 1932, available: true }, { _id: 5, title: "The Catcher in the Rye", author_id: 5, genres: ["Realist Novel", "Bildungsroman"], published_year: 1951, available: true }, { _id: 6, title: "Moby-Dick", author_id: 6, genres: ["Adventure Fiction"], published_year: 1851, available: true }, { _id: 7, title: "Pride and Prejudice", author_id: 7, genres: ["Romantic Novel"], published_year: 1813, available: true }, { _id: 8, title: "War and Peace", author_id: 8, genres: ["Historical Novel"], published_year: 1869, available: true }, { _id: 9, title: "Crime and Punishment", author_id: 9, genres: ["Philosophical Novel"], published_year: 1866, available: true }, { _id: 10, title: "The Hobbit", author_id: 10, genres: ["Fantasy"], published_year: 1937, available: true } ])

the outcomaes should be as follows below after you press Enter:

  acknowledged: true,
  insertedIds: {
    '0': 1,
    '1': 2,
    '2': 3,
    '3': 4,
    '4': 5,
    '5': 6,
    '6': 7,
    '7': 8,
    '8': 9,
    '9': 10
  }

 db.AuthorsCollection.insertMany([ { _id: 1, name: "George Orwell", nationality: "British", birth_year: 1903, death_year: 1950 }, { _id: 2, name: "Harper Lee", nationality: "American", birth_year: 1926, death_year: 2016 }, { _id: 3, name: "F. Scott Fitzgerald", nationality: "American", birth_year: 1896, death_year: 1940 }, { _id: 4, name: "Aldous Huxley", nationality: "British", birth_year: 1894, death_year: 1963 }, { _id: 5, name: "J.D. Salinger", nationality: "American", birth_year: 1919, death_year: 2010 }, { _id: 6, name: "Herman Melville", nationality: "American", birth_year: 1819, death_year: 1891 }, { _id: 7, name: "Jane Austen", nationality: "British", birth_year: 1775, death_year: 1817 }, { _id: 8, name: "Leo Tolstoy", nationality: "Russian", birth_year: 1828, death_year: 1910 }, { _id: 9, name: "Fyodor Dostoevsky", nationality: "Russian", birth_year: 1821, death_year: 1881 }, { _id: 10, name: "J.R.R. Tolkien", nationality: "British", birth_year: 1892, death_year: 1973 } ])

  acknowledged: true,
  insertedIds: {
    '0': 1,
    '1': 2,
    '2': 3,
    '3': 4,
    '4': 5,
    '5': 6,
    '6': 7,
    '7': 8,
    '8': 9,
    '9': 10
  }

   db.PatronsCollection.insertMany([ { _id: 1, name: "Alice Johnson", email: "alice@example.com", borrowed_books: [] }, { _id: 2, name: "Bob Smith", email: "bob@example.com", borrowed_books: [1, 2] }, { _id: 3, name: "Carol White", email: "carol@example.com", borrowed_books: [] }, { _id: 4, name: "David Brown", email: "david@example.com", borrowed_books: [3] }, { _id: 5, name: "Eve Davis", email: "eve@example.com", borrowed_books: [] }, { _id: 6, name: "Frank Moore", email: "frank@example.com", borrowed_books: [4, 5] }, { _id: 7, name: "Grace Miller", email: "grace@example.com", borrowed_books: [] }, { _id: 8, name: "Hank Wilson", email: "hank@example.com", borrowed_books: [6] }, { _id: 9, name: "Ivy Taylor", email: "ivy@example.com", borrowed_books: [] }, { _id: 10, name: "Jack Anderson", email: "jack@example.com", borrowed_books: [7, 8] } ])

  acknowledged: true,
  insertedIds: {
    '0': 1,
    '1': 2,
    '2': 3,
    '3': 4,
    '4': 5,
    '5': 6,
    '6': 7,
    '7': 8,
    '8': 9,
    '9': 10
  }

  To Find All Books use the following command :

  LibraryDB> db.BooksCollection.find()

  and the Outcomes are as follows below :

  [
  {
    _id: 1,
    title: '1984',
    author_id: 1,
    genres: [ 'Dystopian', 'Political Fiction' ],
    published_year: 1949,
    available: true
  },
  {
    _id: 2,
    title: 'To Kill a Mockingbird',
    author_id: 2,
    genres: [ 'Southern Gothic', 'Bildungsroman' ],
    published_year: 1960,
    available: true
  },
  {
    _id: 3,
    title: 'The Great Gatsby',
    author_id: 3,
    genres: [ 'Tragedy' ],
    published_year: 1925,
    available: true
  },
  {
    _id: 4,
    title: 'Brave New World',
    author_id: 4,
    genres: [ 'Dystopian', 'Science Fiction' ],
    published_year: 1932,
    available: true
  },
  {
    _id: 5,
    title: 'The Catcher in the Rye',
    author_id: 5,
    genres: [ 'Realist Novel', 'Bildungsroman' ],
    published_year: 1951,
    available: true
  },
  {
    _id: 6,
    title: 'Moby-Dick',
    author_id: 6,
    genres: [ 'Adventure Fiction' ],
    published_year: 1851,
    available: true
  },
  {
    _id: 7,
    title: 'Pride and Prejudice',
    author_id: 7,
    genres: [ 'Romantic Novel' ],
    published_year: 1813,
    available: true
  },
  {
    _id: 8,
    title: 'War and Peace',
    author_id: 8,
    genres: [ 'Historical Novel' ],
    published_year: 1869,
    available: true
  },
  {
    _id: 9,
    title: 'Crime and Punishment',
    author_id: 9,
    genres: [ 'Philosophical Novel' ],
    published_year: 1866,
    available: true
  },
  {
    _id: 10,
    title: 'The Hobbit',
    author_id: 10,
    genres: [ 'Fantasy' ],
    published_year: 1937,
    available: true
  }
]

to find a specific book by Title use the following commad :

db.BooksCollection.find({title: "To Kill a Mockingbird"})

The outcomes will be as follows below:

[
  {
    _id: 2,
    title: 'To Kill a Mockingbird',
    author_id: 2,
    genres: [ 'Southern Gothic', 'Bildungsroman' ],
    published_year: 1960,
    available: true
  }
]

To find Find All Books by a Specific Author use the following command:

 db.BooksCollection.find({author_id: 5})

 Outcomes will be as follows: 

 [
  {
    _id: 5,
    title: 'The Catcher in the Rye',
    author_id: 5,
    genres: [ 'Realist Novel', 'Bildungsroman' ],
    published_year: 1951,
    available: true
  }
]

to find all the Available books use the following commad:

 db.BooksCollection.find({available: true})

 UPDATE:

 update Book availability using $set use the following commad :

 db.BooksCollection.updateOne({ _id: 3 }, { $set: { available: false } })

 outcome:

 {
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
}

add genre to Book $addToSet

db.BooksCollection.updateOne({ _id: 8 }, { $addToSet: { genres: "Epic" } })

Add a borrowed book to a patron’s record (_id: 5)



 Advanced Queries with Operators


Find Books Published After 1950 (Using $gt)

db.BooksCollection.find({ published_year: { $gt: 1950 } })

Find All American Authors (Using $eq)

db.AuthorsCollection.find({ nationality: { $eq: "American" } })

Find All Books That Are Available And Published After 1950

 db.BooksCollection.find({ available: true, published_year: { $gt: 1950 } })

Find authors whose names contain "George" (Using $regex)

db.AuthorsCollection.find({ name: { $regex: /George/ } })

Increment the published year of "1869" by 1 (Using $inc)

db.BooksCollection.updateOne({ published_year: 1869 }, { $inc: { published_year: 1 } })

Set All Books To Available (Using $set)

db.BooksCollection.updateMany({}, { $set: { available: true } })
 