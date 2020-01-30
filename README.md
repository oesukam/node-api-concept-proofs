## Node/Express API proofs of concepts

In this project, you are part of a team building a blog platform. One requirement is for a REST API service to provide posts information using the Nodejs Express framework. The requirements include filtering and ordering requirements, response codes and error messages for the queries you must implement.

The definitions and a detailed requirements list follow. You will be graded on whether your application performs data retrieval and manipulation based on given use cases exactly as described in the requirements.

### Features
#### Required features
-   Users should be able to add a new post
-   Users should be able to update a single post
-   Users should be able to retrieve a sinle post
-   Users should be able to delete a single post
-   Users should be able to retrive all posts

#### Optional features
-   Order posts by title, description, created date, etc.
-   Filter post by title, description, etc.
  
### Schema
-   Post
  ```js
    {
      id: String|Required,
      slug: String|Required,
      poster: String|Required,
      title: String|Required,
      description: String|Required,
      createdAt: Date|Required,
      updatedAt: Date|Required,
    }
  ```
### Responses
#### Generic Responses
-   Success reposnse
  ```js
    {
      status: Integer,
      message: String,
      data: Object|Array
    }
  ```

-   Error response
  ```js
  {
    status: Integer,
    error: Object|Array
  }
  ```

#### Success Posts response
-   POST /posts
  ```js
  {
    status: 201,
    data : {
      id: String|Required,
      slug: String|Required,
      poster: String|Required,
      title: String|Required,
      description: String|Required,
      createdAt: Date|Required,
      updatedAt: Date|Required,
    }
  }
  ```
-   POST /posts/postId
  ```js
  {
    status: 200,
    data : {
      id: String|Required,
      slug: String|Required,
      poster: String|Required,
      title: String|Required,
      description: String|Required,
      createdAt: Date|Required,
      updatedAt: Date|Required,
    }
  }
  ```
-   GET /posts
  ```js
  {
    status: 200,
    data : [
      {
        id: String|Required,
        slug: String|Required,
        poster: String|Required,
        title: String|Required,
        description: String|Required,
        createdAt: Date|Required,
        updatedAt: Date|Required,
      }
    ]
  }
  ```

### Technologies
-   Node/Express
-   Mongodb
-   Jest/Supertest


### Recommended packages
-   [Celebrate](https://www.npmjs.com/package/celebrate): celebrate is an express middleware function that wraps the joi validation library
-   [Mongoose](https://www.npmjs.com/package/mongoose): Mongoose is a MongoDB object modeling tool designed to work in an asynchronous environment.
-   [Babel-watch](https://www.npmjs.com/package/babel-watch): Reload your babel-node app on JS source file changes. And do it fast.


### Acceptance criteria
-   You should setup babel and use es6 features
-   All the endpoints should work as expected
-   Some endpoints should have request validation
-   You should write integration tests for all endpoints
-   Features should be implemented in different branches

### Basic Project Structure
[Project Structure](./project-structure)
### Author
-   [Olivier Esuka](https://github.com/oesukam)
