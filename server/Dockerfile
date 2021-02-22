FROM elixir:1.11.3

WORKDIR /app/rocketpay

RUN mix local.hex --force \
  && mix archive.install --force hex phx_new 1.5.7 \
  && mix local.rebar --force

EXPOSE 4000

CMD ["mix", "phx.server"]