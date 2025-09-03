# NuxGame Test Work

This is a test project created by Oleh Miestiechkin for NuxGame IT company.

The website allows you to register and, after registration, receive a unique link to a special page.  
The link is valid for 7 days.

On this page, you can play a simple game:

- Click the "I'm feeling lucky" button to get a random number between 1 and 900.
- If the number is even — you win.
- If the number is odd — you lose.

Other features of the game you can explore on your own.

---

## Requirements

- PHP 8.3
- Composer
- Laravel 11.42
- SQLite

---

## Installation

The repository already contains a `Dockerfile`, `docker-compose.yml`, and `.env` file.

Run the following commands:

```bash
git clone https://github.com/Yurservice/NuxGame.git project
cd project
docker compose up -d --build
docker compose exec php-fpm composer install
docker compose exec php-fpm php artisan key:generate
docker compose exec php-fpm php artisan migrate
docker compose exec php-fpm php artisan serve --host=0.0.0.0 --port=8000
```
Now open:
http://localhost:8000