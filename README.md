## STEPS TO CREATE DEV ENVIRONMENT:

### 1 - Create the container manually with the following command:

    `docker run --rm -it -v $(pwd)/server:/app  -p 4000:4000 elixir:1.11.3 bash`

### 2 - Install the phx_new:

    `mix local.hex --force && mix archive.install --force hex phx_new 1.5.7`

### 3 - Create the project:

    `mix phx.new /app/rocketpay --no-webpack --no-html`

### 4 - Run docker-compose:

    `docker-compose up -d --build`

 **Note:** the parameter **--build** in docker-compose is only needed when making changes to the project's **Dockerfile** or **docker-compose.yaml** file.

 Enjoy the project and if it helped you, stars are welcome :)


