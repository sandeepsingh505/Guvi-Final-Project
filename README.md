<h1 align="center">
    <br>
    Library Management System
    <br>
</h1>


[![Spring Boot](https://img.shields.io/badge/Spring-6DB33F?style=for-the-badge&logo=spring&logoColor=white)]()
[![Angular](https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white)]()
[![MySQL](https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white)]()
[![Hibernate](https://img.shields.io/badge/Hibernate-59666C?style=for-the-badge&logo=Hibernate&logoColor=white)]()
[![Maven](https://img.shields.io/badge/apache_maven-C71A36?style=for-the-badge&logo=apachemaven&logoColor=white)]()
[![Bootstrap](https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white)]()

A full stack application using Spring Boot, Angular and MySQL. 
* This is a Library Management System with an Admin and a User side for the application. 
* Admin can perform CRUD with books/users. 
* User can borrow and return a book. 
* Uses JWT to authenticate login.
* Uses BCryptPasswordEncoder to encrypt the password stored in the database.
* Redirects to forbidden page if a role doesn't have access to the url.
<br>

# APIs

## Authenticate
* Post Mapping to return JWT.
```
{
    username: "user",
    password: "password"
}
```

## Book
* Get Mapping to find all books in the database.
* Get Mapping to find book by id provided.
* Post Mapping to create book.
```
{
    "bookName": "Book Name",
    "bookAuthor": "Author Name",
    "bookGenre": "Genre",
    "noOfCopies": 5
}
```
* Put Mapping to edit book.
```
{
    "bookName": "New Book Name",
    "bookAuthor": "Author Name",
    "bookGenre": "Genre",
    "noOfCopies": 7
}
```
* Delete Mapping to delete a book.

## User
* Get Mapping to find all users in the database.
* Get Mapping to find user by id provided.
* Post Mapping to create user.
```
{
    "username": "user",
    "name": "First User",
    "password": "password",
    "role": [
        {
            "roleName": "Admin"
        }
    ]
}
```
* Put Mapping to edit user.
```
{
    "username": "user",
    "name": "New First User",
    "password": "password",
    "role": [
        {
            "roleName": "User"
        }
    ]
}
```

## Borrow
* Get Mapping to find all transactions taken place.
* Get Mapping to find list of books borrowed by a user.
* Get Mapping to find list of users who have borrowed a particular book.
* Post Mapping to borrow a book.
```
{
    "bookId": 3,
    "userId": 5
}
```
* Post Mapping to return a book.
```
{
    "borrowId": 1
}
```

<br>

# Screenshots

## Home & Login
### Home
![home](https://github.com/user-attachments/assets/3c17cfc9-4809-4532-9535-7a8044a083cf)


### Login
![login](https://github.com/user-attachments/assets/088087af-e143-4b27-8ad4-c88673fdeae7)


## Admin
### All books present
![book_list](https://github.com/user-attachments/assets/c325f7c4-5461-463e-9259-b19f658e07d3)


### Adding a book
![book_add](https://github.com/user-attachments/assets/4a3ca309-cb2a-4ee2-bf38-361d4d15b201)


### Updating book details
![book_update](https://github.com/user-attachments/assets/a86fe450-5987-4c07-8927-4aee606b2ddf)


### Borrow history of a book
![book_details](https://github.com/user-attachments/assets/b12d89ba-2161-48e8-9694-55f1a4372c4e)


### All users present
![user_list](https://github.com/user-attachments/assets/87453f61-4bda-4021-a003-0d2ce0fc3bf6)


### Adding a user
![user_add](https://github.com/user-attachments/assets/5856960a-69e0-4c4c-9000-3f8748746980)


### Borrow history to the user
![user_details](https://github.com/user-attachments/assets/c3ef4460-d8b8-4152-bd18-4aedf67fb03f)


## User
### Borrow book
![borrow_book](https://github.com/user-attachments/assets/1a16b759-2f93-4e3c-85b8-79770e5dad17)


### Return book
![return_book](https://github.com/user-attachments/assets/e785588e-d9d3-45f8-a71d-10662d11f374)


### Forbidden
![forbidden](https://github.com/user-attachments/assets/ee6a3602-705c-4b6e-af4c-e88019785268)


<br>

# Application Properties
```
server.port = yourPreferredPortNumber

spring.datasource.url = jdbc:mysql://localhost:3306/yourSchemaName
spring.datasource.username = yourUsername
spring.datasource.password = yourPassword
```

# Development
* Frontend
```
npm install
```
* Backend
```
mvn install
```

# Build
* Frontend
```
ng serve
```

* Backend
```
mvn spring-boot:run
```
