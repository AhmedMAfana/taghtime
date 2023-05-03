# ![Tagh Time App](logo.png)


# Getting started

## Installation

Clone the repository

    git clone git@gitlab.com:amidigital/Tagh-Time.git

Switch to the repo folder

    cd Tagh-Time

Install all the dependencies using composer

    composer install --no-scripts --ignore-platform-reqs


Copy the example env file and make the required configuration changes in the .env file


    cp .env.example .env


Start the local development server relying on [Docker](#docker).

    sail up
 
You can now access the server at http://0.0.0.0


Access Docker bash for package

    docker exec -it tagh-time-php-fpm-1 bash
    
Switch to the repo folder

     cd laravel/current/


Generate a new application key

    php artisan key:generate


Run the database migrations

    artisan migrate:fresh --path=/database/migrations/company
 
 Run the database seeders
 
     php artisan db:seed --class=Database\\Seeders\\Company\\PlanSeeder

 
