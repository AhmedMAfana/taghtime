# ![Tagh Time App](logo.png)


# Getting started with Back-end in localhost

## Installation

Clone the repository

    git clone git@gitlab.com:amidigital/Tagh-Time.git

Switch to the repo folder

    cd Tagh-Time


Switch to the master branch

    git checkout master
    
Install all the dependencies using composer

    composer install --no-scripts --ignore-platform-reqs


Copy the example env file and make the required configuration changes in the .env file


    cp .env.example .env


Start the local development server relying on [Docker](#docker).

    sail up
 

Access Docker bash for package

    docker exec -it tagh-time-php-fpm-1 bash
    
Switch to the repo folder

     cd laravel/current/


Generate a new application key

    php artisan key:generate


Run the database migrations

     php artisan migrate:fresh --path=/database/migrations/company

 Run the database seeders
 
     php artisan db:seed --class=Database\\Seeders\\Company\\PlanSeeder

  

You can now access the server at http://localhost

## configuration queue work by supervisor
