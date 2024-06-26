# API

## Getting Started

### Docker

1. Open a terminal and go to: `./docker-compose-intro`
2. Run the command: `docker-compose up`
3. Run a HTTP request to `http://localhost:8000/users`

If you see several records as output of the request your application is runnung successfuly.

## Routes

GET /users

Returns all users in mongodb collection

GET /users?first_name={person_name}

Returns all users which match with the first name

GET /users/:id

Finds user by id - must be a valid mongoObjectId

POST /users

Create an user, the express app autogenerates the Id

**Body**
```
"first_name": "Brandise",
  "last_name": "Ingerman",
  "email": "bingerman0@youku.com",
  "gender": "Female",
  "address": {
    "city": "Fresno",
    "state": "California",
    "country": "United States",
    "country_code": "US"
  },
  "card": {
    "card_number": "3571237735836521",
    "card_type": "jcb",
    "currency_code": "USD",
    "balance": "$630.16"
  },
  "married_status": true
```


PUT /users/:id

Updates an user

**Body**
```
"first_name": "Brandise",
  "last_name": "Ingerman",
  "email": "bingerman0@youku.com",
  "gender": "Female",
  "address": {
    "city": "Fresno",
    "state": "California",
    "country": "United States",
    "country_code": "US"
  },
  "card": {
    "card_number": "3571237735836521",
    "card_type": "jcb",
    "currency_code": "USD",
    "balance": "$630.16"
  },
  "married_status": true
```


DELETE /users/:id

Deletes an user by id