## Rocketpay app - A project of the week NLW 4 by Rocketseat

This project is part of a personal challenge to implement a Elixir application completely free of installations on the host machine, all via docker.
## STEPS TO CREATE DEV ENVIRONMENT:

### 1 - Create the container manually with the following command:

    docker run --rm -it -v $(pwd)/server:/app  -p 4000:4000 elixir:1.11.3 bash

### 2 - Install the phx_new:

    mix local.hex --force && mix archive.install --force hex phx_new 1.5.7

### 3 - Create the project:

    mix phx.new /app/rocketpay --no-webpack --no-html

### 4 - Exit the container and adjust the permissions of the project directory with your user:

    sudo chown -R yourusername:yourusergroup server

### 5 - Enable execution permission to entrypoint file:

    chmod +x server/entrypoint.sh

### 6 - Run docker-compose passing user id and group id with script:

    sh start.sh

### Note!
    In case of permission error with the _build directory, run the command "chown -R youruser:yourgroup _build" again.

 Enjoy the project and if it helped you, stars are welcome :)


