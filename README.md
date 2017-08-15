# Docker Symfony (PHP7-FPM - NGINX ...)

## Install / Launch server

1. Create a `.env` from the `.env.dist` file. Adapt it according to your symfony application

    ```bash
    cp .env.dist .env
    ```

1. Create a `docker-compose.yml` from the `docker-compose.yml.dist` file. Adapt it according to your symfony application

    ```bash
    cp docker-compose.yml.dist docker-compose.yml 
    ```

2. Build and run containers

    ```bash
    $ ./run
    ```

## Useful commands

You can use the shortcut "exec" (= sudo docker-compose exec --user www-data php "$@")

    ```bash
    # Bash 
    $ ./exec bash
    # Composer
    $ ./exec composer update 
    # Symfony2
    $ ./exec sf doctrine:database:create 
    # Symfony3
    $ ./exec sf3 doctrine:database:create 
    ```

## Customize

If you want to add optionnals containers like Redis, PHPMyAdmin... update your docker-compose.yml

## Contributing

This project is forked from https://github.com/maxpou/docker-symfony

First of all, **thank you** for contributing ♥  
While creating your Pull Request on GitHub, please write a description which gives the context and/or explains why you are creating it.
