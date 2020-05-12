# Record Shop

## Task 01 - Mock database and Controllers

Most applications made for the web have to do with some sort of data manipulation. In order to be able to manipulate our data we have to do two things first:

    - We need to define the endpoints of our app that our users will use to send
      different kinds of requests (GET, POST, DELETE, etc).
    - We have to define how do we want our data to look like and of course store them somewhere.

**Story**: Our client is a record shop owner who wants to have a list of products in the main page of their shop. They know that they want to display the title, the artist, the year, the cover image and the price for each record they have available. However, the client still doesn't have a full list of all their products. He would also like to be able to add new records to his collection.

**TODO**:

1. Please create two endpoints (routes) for the shop owner

   - `records` -> a `GET` that will return all records of the store
   - `records` -> a `POST` that will add a new record to the record collection

   For now you can just return a string from the above endpoints, just to make sure everything works.

2. Using `lowdb` set up a mock database for our records. It can be empty or it can contain already some fake data. Update the routes above so that they work just like they should.

   - `records` -> should return all the records that are in our lowdb database
   - `records` -> should add a new record to our lowdb database

## Task 02 - Middleware and CORS

Middleware functions are functions that have access to the request object (req), the response object (res), and the next middleware function in the application’s request-response cycle. The next middleware function is commonly denoted by a variable named `next`. There are a number of already made middleware functions we can use and we can also build our own custome middleware functions. You can already see that by default your express app is already using `morgan` and `express.json()` as it's middleware.

Cross-Origin Resource Sharing (CORS) is a mechanism that uses additional HTTP headers to tell browsers to permit a web application running at one origin access selected resources from a different origin. A web application executes a cross-origin HTTP request when it requests a resource that has a different origin (domain, protocol, or port) from its own.

**TODO**:

1. Write your own middleware to allow CORS check out the (example we made)[https://github.com/dci-ber-fbw21/cors-with-express/commit/4ad9d04868bf83e9b8a20856340bbf2a273442ab]
2. Please use [CORS Middleware](https://github.com/expressjs/cors) in this application to allow requests from other origins.
