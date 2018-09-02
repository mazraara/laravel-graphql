# laravel-graphql

A simple app to try out GraphQL using Laravel with SQLite

```bash
composer install
```

Duplicate `.env.example` and rename it `.env`

Add full path to SQL lite 

`DB_CONNECTION=sqlite`

`DB_DATABASE=/app/laravel-graphql/database/database.sqlite`

Then run:

```bash
php artisan key:generate
```

Then create the tables by running:

```bash
php artisan migrate
```

And finally, start the application:

```bash
php artisan serve
```

now visit [http://localhost:8000/graphiql](http://localhost:8000/graphiql) to see the application running.

Example of API call

http://localhost:8000/graphiql?query={
  tasks {
    id
    title
    is_completed
  }
}

A similar REST API endpoint will be like 

http://localhost:8000/tasks/


This will respond 

`{
  "data": {
    "tasks": [
      {
        "id": 1,
        "title": "Earum aut voluptatem fugit officia qui.",
        "is_completed": false
      },
      {
        "id": 2,
        "title": "Repellat eos sint enim pariatur odio et deserunt.",
        "is_completed": false
      },
      {
        "id": 3,
        "title": "Aut eius ad consequatur eveniet rerum.",
        "is_completed": false
      },
    ]
  }
}`


Acknowledgments

https://github.com/Folkloreatelier/laravel-graphql