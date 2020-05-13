## Docker environment for laravel 7.0

## Requires

- docker v19.03.8
- docker-compose v1.25.4

## How to start

In terminal:
- git clone https://github.com/EugeneGpil/DockerLaravel.git DockerLaravel
- cd DockerLaravel
- laravel new project (or get fresh laravel project using composer)
- mkdir databases

Open project/.env file and set database connection:

- DB_CONNECTION=mysql
- DB_HOST=127.0.0.1
- DB_PORT=3306
- DB_DATABASE=NewLaravelDatabase
- DB_USERNAME=root
- DB_PASSWORD=123

Back to terminal:
- docker-compose up --build

In browser:
- open localhost:6080
- login with root 123
- create new database "NewLaravelDatabase"

In terminal:
- docker-compose exec php bash
- php artisan key:generate
- php artisan migrate

In browser:
- open localhost:8080