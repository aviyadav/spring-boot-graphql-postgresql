# Spring Boot + GraphQL + PostgreSQL example

For more detail, please visit:
> [Spring Boot + GraphQL + PostgreSQL example](https://www.bezkoder.com/spring-boot-graphql-postgresql/)

## Run Spring Boot application
```
mvn spring-boot:run
```

POST - http://localhost:8080/apis/graphql

Body
    GraphQL
    schema - auto-fetch


### CRUD GraphQL APIs
 Create an Author:

- GraphQL

>    mutation {
    createAuthor(
        name: "bezkoder",
        age: 27) {
        id name
    }
    }


– Create a Tutorial:

GraphQL: we want response including Tutorial id, title and author (name)

mutation {
  createTutorial (
    title: "Tutorial #1",
    description: "Description for Tut#1"
    author: 1)
    {
      id title author { name }
    }
}

– Read all Authors:

GraphQL
{
  findAllAuthors{
    id
    name
    age
  }
}

– Read all Tutorials:

GraphQL
{
  findAllTutorials{
    id
    title
    description
    author{
      id
      name
    }
  }
}

– Update a Tutorial:

GraphQL
mutation {
  updateTutorial (
    id: 2
    description: "updated Desc Tut#2")
    {
      id title description author { name }
    }
}

– Delete a Tutorial:

GraphQL
mutation {
  deleteTutorial(id: 1)
}

– Count number of Tutorials:

GraphQL
{
  countTutorials
}
