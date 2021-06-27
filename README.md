# TodoList

**Table of Contents**

- [TodoList](#todolist)
  - [Required](#required)
  - [Run App](#run-app)
  - [Api Reference](#api-reference)
    - [Get All Todo](#get-all-todo)
    - [Get Todo by Id](#get-todo-by-id)
    - [Post Todo](#post-todo)
    - [Update Todo](#update-todo)
    - [Delete Todo](#delete-todo)

## Required

java >= 11

```sh
java -version
```

## Run App

```sh
./gradlew bootrun
```

## Api Reference

### Get All Todo

| method | path  |
| :----- | :---- |
| get    | /todo |

example
```sh
curl -x get http://localhost:8080/todo
```

### Get Todo by Id

| method | path       |
| :----- | :--------- |
| get    | /todo/{id} |

example
```sh
curl -x get http://localhost:8080/todo/1
```

### Post Todo

| method | path  |
| :----- | :---- |
| post   | /todo |

```sh
curl -x post http://localhost:8080/todo \
 -h `content-type: application/json` \
 -d '{"name": "new todo"}'
```

### Update Todo

| method | path       |
| :----- | :--------- |
| post   | /todo/{id} |

```sh
curl -x put http://localhost:8080/todo/1 \
 -h `content-type: application/json` \
 -d '{"name": "new name"}'
```

### Delete Todo

| method | path       |
| :----- | :--------- |
| delete | /todo/{id} |

```sh
curl -x delete http://localhost:8080/todo/1
```