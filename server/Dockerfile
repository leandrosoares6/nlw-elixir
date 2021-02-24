FROM elixir:1.11.3

RUN apt-get update && \
  apt-get install -y postgresql-client

RUN mix local.hex --force \
  && mix archive.install --force hex phx_new 1.5.7 \
  && mix local.rebar --force

WORKDIR /app/rocketpay

COPY . .

EXPOSE 4000

CMD ["/app/entrypoint.sh"]