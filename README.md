<h1 align='center'>📣 Slim API</h1>
<blockquote align='center'>An API made with Slim Framework, a framework for PHP that helps you create APIs.</blockquote>

## 💡What is it?
Slim API is and simples API made during the Web Development course to study the Slim framework, a framework for PHP that helps you to create APIs.

## 💾 Configure database
To run this application you first need to configure your database.
- Download xampp on your computer (or another software you like) and run Apache and mysql.

- Go to `localhost:phpmyadmin` and create a database called `slim`.

- Open a terminal and go to your project folder, run `php db.php` to create your database and configure it.

- Open an terminal and go to the public folder of the project, run `php -S localhost:<port>` to open the server.

## ✒ Routes
`localhost:<port>/api/token` -> Generates a token based on the parameters sent to it. You will need to send an email and a password in the body of the request (you need to add a user to your `usuarios` table in phpadmin). The token is used on the routes below for authentication, on all routes you need to send a header called `X-Token` with the token.

❗ *The following routes come after `localhost:<port>/api/v1`.*

- GET `/produtos/lista` -> List all products registered in your database.

- POST `/produtos/adiciona` -> Create a new product and add it to your database. To do this, you must send in the body of the request a form with a title (as 'titulo'), description (as 'descricao'), price (as 'preco') and manufacturer (as 'fabricante').

- GET `/produtos/lista/{id}` -> List an specific product based on it id.

- PUT `/produtos/atualiza/{id}` -> Update an product based on it it. To do this, you must send in the body of the request a form with the columns you want to update, they can be: title (as 'titulo'), description (as 'descricao'), price (as 'preco') and manufacturer (as 'fabricante').

- DELETE `/produtos/remove/{id}` -> Delete an specific product based on it id.

## 🚧Built With
- PHP
- MySql
- Slim Framework
- HTML
- CSS
