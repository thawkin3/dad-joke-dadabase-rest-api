# Dad Joke "Dadabase" REST API

Groan at some dad jokes and rate them as well. Which joke will be your favorite?

This API is built with [JSON Server](https://github.com/typicode/json-server). It provides the backend service for the Dad Joke Dadabase app found here: https://github.com/thawkin3/dad-joke-dadabase

## Running the app locally

1. `npm install`
2. `npm start`

This will start the json-server API on port 3000.

## REST API with json-server

### Database

```
# See the current database contents
GET /db
```

### Jokes

```
GET    /jokes
GET    /jokes/1
POST   /jokes
PUT    /jokes/1
PATCH  /jokes/1
DELETE /jokes/1

# Get a specific joke with all ratings included
GET /jokes/1?_embed=ratings

# Get all ratings for a specific joke
GET /jokes/1/ratings

# Get all jokes with all ratings included
GET /jokes?_embed=ratings
```

### Ratings

```
GET    /ratings
GET    /ratings/1
POST   /ratings
PUT    /ratings/1
PATCH  /ratings/1
DELETE /ratings/1

# Get all ratings for a specific joke
GET /ratings?jokeId=1

# Get a rating along with the joke itself
GET /ratings/1?_expand=joke
```
