# Laravel 8 REST API with Sanctum Authentication

This project is a Laravel 8 REST API with authentication powered by Laravel Sanctum. It provides endpoints for managing products and user authentication.

## Introduction

This API project is built using Laravel 8 and offers a secure authentication mechanism using Laravel Sanctum. It allows users to register, log in, and perform CRUD operations on products.

## Features

- User registration and login.
- Token-based authentication using Laravel Sanctum.
- Create, read, update, and delete operations for products.
- Search products by name.

## Requirements

- PHP >= 8.1
- Composer
- Laravel CLI
- MySQL or another supported database

## Project structure

```
$PROJECT_ROOT
├── App
    ├── Console
    ├── Exceptions
    ├── Http
        ├── Controllers
            ├── AuthConroller.php #Authentication controller 
            ├── Controller.php
            ├── ProductController.php #Product Controller
        ├── Middleware
        └── Kernel.php
    ├── Models
        ├── Product.php #the model for product
        └── User.php #the model form user
    └── Providers
├── bootstrap
├── config
├── databases
    ├── factories
    ├── migrations
        ├── 2014_10_12_000000_create_users_table.php #the user table
        ...
        └── 2023_08_26_123852_create_products_table.php # the product table
    └── seeders
├── public
├── resources
├── routes
    ├── api.php #the api routes
    ...
    └── web.php
├── storage
├── test 
├── vendor  
└── .env # database configurations
...
```

## Installation

1. Clone the repository:
```
https://github.com/elmahdibouaiti/authentication.git
```

```
cd authentication
```
2. Install dependencies:

```
composer install
```


3. Copy the `.env.example` file to `.env` and configure your environment variables, including your database settings and app key.

4. Generate the application key:
```
php artisan key:generate
```


5. Run migrations:
```
php artisan migrate
```


6. Start the development server:
```
php artisan serve
```

## Usage

- Register a user: POST to `/register`
- Log in: POST to `/login`
- Log out (authenticated): POST to `/logout`
- List all products: GET to `/products`
- Get product by ID: GET to `/products/{id}`
- Search products by name: GET to `/products/search/{name}`
- Create a product (authenticated): POST to `/products`
- Update a product (authenticated): PUT to `/products/{id}`
- Delete a product (authenticated): DELETE to `/products/{id}`

Remember to use tools like Postman or CURL to interact with the API.

## Authentication

- To authenticate, use the `Bearer` token in the Authorization header.
- After successful login, the API will provide an access token.

## Error Handling

The API follows RESTful conventions and provides appropriate HTTP status codes and error messages for various scenarios. Refer to the documentation for details on error responses.

## Contributing

Contributions are welcome! Feel free to fork this repository, make improvements, and submit a pull request.

## Credits

https://laravel.com/docs/8.x/sanctum

---


