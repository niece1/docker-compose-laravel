# docker-compose-laravel
Usage
To get started, make sure you have Docker installed on your system, and then clone this repository.

Add your entire Laravel project to the src folder, then open a terminal and from this cloned respository's root run docker-compose up -d --build. Open up your browser of choice to http://localhost:8080 and you should see your Laravel app running as intended.

New: Three new containers have been added that handle Composer, NPM, and Artisan commands without having to have these platforms installed on your local computer. Use the following command templates from your project root, modifiying them to fit your particular use case:

docker-compose run --rm composer update
docker-compose run --rm npm run dev
docker-compose run --rm artisan migrate
Containers created and their ports (if used) are as follows:

nginx - :8080
mysql - :3306
php - :9000
npm
composer
artisan
