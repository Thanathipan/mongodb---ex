# MongoDB Movie Database

##1. Create a Database called `movies`
```javascript
use movies

##2. Create a Collection called moviedetails


db.createCollection("moviedetails")

##3. Insert 5 Movie Documents into the moviedetails Collection


db.moviedetails.insertMany([
    { "title": "Vikram", "genre": "Drama", "director": "Lokesh Kanakaraj", "releaseYear": 2022 },
    { "title": "Vettaiyan", "genre": "Action", "director": "Ganavel", "releaseYear": 2024 },
    { "title": "Kanguva", "genre": "Fantasy", "director": "Siva", "releaseYear": 2025 },
    { "title": "Leo", "genre": "Action", "director": "Lokesh Kanakaraj", "releaseYear": 2023 },
    { "title": "Vidamuyatchi", "genre": "Thriller", "director": "Magizh Thirumeni", "releaseYear": 2025 }
])

##4. List All Documents Created



db.moviedetails.find().pretty()

##5. List Movies Directed by Lokesh Kanakaraj



db.moviedetails.find({ "director": "Lokesh Kanakaraj" }).pretty()

##6. List Lokesh Kanakaraj’s Movies Released in 2023



db.moviedetails.find({ "director": "Lokesh Kanakaraj", "releaseYear": 2023 }).pretty()

##7. Delete the Movie You Don’t Like



db.moviedetails.deleteOne({ "title": "Movie Title" })

##8. Add Your Favorite Movie



db.moviedetails.insertOne({
    "title": "Your Favorite Movie Title",
    "genre": "Your Favorite Genre",
    "director": "Director's Name",
    "releaseYear": 202X
})

##9. List the Movie Directed by Magizh Thirumeni in 2025


db.moviedetails.find({ "director": "Magizh Thirumeni", "releaseYear": 2025 }).pretty()

##10. List Out the Directors’ Names in Your Document


db.moviedetails.distinct("director")



