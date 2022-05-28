docker-symfony-postgre-min
--------------------------
Minimal Docker configuration with `PHP 8.1`, `NGINX 1.20+`, `PostgreSQL 14.2+` and `Symfony 6` for development.

Initialization
====================================================

1. Clone the project:
   
        git clone https://github.com/arturmazanik/docker-symfony-postgre-min.git

1. Go to the project's folder
   
        cd /path/to/docker-symfony-postgre-min
   
1. Build and up project with Docker Compose

        docker-compose up -d --build
   
1. Run the docker exec command. To do that, run the command below

        docker-compose exec php /bin/bash

1. setup meets the requirements for a Symfony application by running the following command
   
        symfony check:requirements
   You will see the following output in the terminal:
   
         [OK]
         Your system is ready to run Symfony projects
   
1. create a new Symfony project by running the following command
   
         symfony new .
   If successful, you will see the following text in the terminal output

        [OK] Your project is now ready in /var/www/symfony_docker
   
1. Open `http://localhost:8080/` in your browser, you should see the Symfony's welcome page.

*For closing docker exec cli you must enter `exit` to command line*

Using
==============

Using Docker Compose
--------------------

Build and up:

      docker-compose up -d --build
Up only:

      docker-compose up -d
Down:

      docker-compose down