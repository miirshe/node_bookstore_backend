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

#### If You Want to Create New Owner and Enter ``Email`` Already Exist the Response You Get Is : 

````markdown
STATUS CODE : `404`,
MESSAGE : `User Already exists`
````


#### If You Want to Login Owner and Enter ``Email`` or ``Password`` Not Exists into the ``db``  the Response You Get Is : 

````markdown
STATUS CODE : `404`,
MESSAGE : `Invalid Email or Password`
````


#### If  Request Body Can Not Reach Into Prisma-client The Reaponse You Get Is : 

````markdown
STATUS CODE : `404`,
MESSAGE : `Something Went Wrong Try Again...`
````

````markdown
Owner Token Is : `ownerToken` storage browser cookies storage
````


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


## Response :

#### If You Want to Create New Author and Enter ``Email`` Already Exist The Response You Get Is : 

````markdown
STATUS CODE : `404`,
MESSAGE : `User Already exists`
````


#### If You Want to Login Author and Enter ``Email`` or ``Password`` Not Exists into the ``db``  the Response You Get Is : 

```markdown
STATUS CODE : `404`,
MESSAGE : `Invalid Email or Password`
```


#### If  Request Body Can Not Reach Into Prisma-client The Reaponse You Get Is : 

````markdown
STATUS CODE : `404`,
MESSAGE : `Something Went Wrong Try Again...`
````

````markdown
Author Token Is : `authorToken` storage browser cookies storage
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




