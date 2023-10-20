# node_bookstore_backend
``This project is a backend application built with Node.js that serves as the foundation for a bookstore management system. It provides a set of APIs to manage owners, bookstores, books, and authors.``


## Features :
````markdown
1.Owner likes register, login, update, delete, fetch
2.Author like register, login, update, delete, fetch
3.Books like add, update, delete, fetch
4.BookStore like add, update, delete, fetch
````


## Owner :

``Owner Endpoints`` 
````markdown
1.``POST Register Owner`` api/owner/register
2.``POST Login Owner ``   api/owner/login
3.``GET Fetch Owners``    api/owners
4.``DELETE Owner ``     api/owner/:id
5.``GET Current Owner`` api/current/owner
````

## Response :

#### if you want to create new owner and enter email already exist the response you get is : 


|  Status Code      |  Message                | 
|  -----------------|-------------------------|
|  `404`            | `User Already exists `  |


#### if you want to login owner and enter email or password not exists into the db  the response you get is : 


|  Status Code      |  Message                      | 
|  -----------------|-------------------------------|
|  `404`            | `Invalid Email or Password `  |


## Owner Fields :

|  Parameter    |  Type   |    Required  |   Description  |
|  ------------ |---------|--------------|----------------|
|  `Username`   | String  | True         | Owner Username 
|  `Email`      | String  | True         | Owner Email only Unique
|  `Password`   | String  | True         | Owner Password


## Author :

``Author Endpoints`` 
````markdown
1.`POST Register Author` api/author/register
2.`POST Login Author `   api/author/login
3.`GET Fetch Authors`    api/authors
4.`DELETE Author `     api/author/:id
5.`GET Current Author` api/current/author
````
## Author Fields :

|  Parameter    |  Type   |    Required  |   Description  |
|  ------------ |---------|--------------|----------------|
|  `name`       | String  | True         | Author name 
|  `Email`      | String  | True         | Author Email only Unique
|  `Password`   | String  | True         | Author Password




## Books :

``Books Endpoints`` 
````markdown
1.``POST Add Book`` api/book/add
2.``GET Fetch Books``    api/books
3.``DELETE Book ``     api/book/:id
4.``PUT Update Book ``     api/book/:id
````
## Book Fields :

|  Parameter           |  Type   |    Required  |   Description  |
|  --------------------|---------|--------------|----------------|
|  `title`             | String  | True         | Book title
|  `price`             | Float   | True         | Book price
|  `image`             | String  | True         | Book Cover Image
|  `bookStoreId`       | String  | True         | Bookstore id



## Bookstore:

``Bookstore Endpoints`` 
````markdown
1.``POST Register Bookstore`` api/bookstore/add
2.``PUT  Update Bookstore``   api/bookstore/:id
3.``GET Fetch Bookstore``    api/bookstore
4.``DELETE Bookstore ``     api/bookstore/:id
````
## Bookstore Fields :

|  Parameter    |  Type   |    Required  |   Description  |
|  ------------ |---------|--------------|----------------|
|  `name`       | String  | True         | Bookstore Name
|  `location`   | String  | True         | Bookstore Location




