FROM elixir:1.11.3

RUN apt-get update && \
  apt-get install -y postgresql-client

ARG USER_ID
ARG GROUP_ID
RUN addgroup --gid $GROUP_ID leandro
RUN adduser --disabled-password --gecos '' --uid $USER_ID --gid $GROUP_ID leandro
USER leandro

WORKDIR /app/rocketpay

RUN mix local.hex --force \
  && mix archive.install --force hex phx_new 1.5.7 \
  && mix local.rebar --force

EXPOSE 4000

CMD ["/app/entrypoint.sh"]

# CMD ["mix", "phx.server"]