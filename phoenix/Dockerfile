FROM elixir:1.7.1

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update \
 && apt-get install -y inotify-tools \
 && apt-get install -y mariadb-client \
 && curl -sL https://deb.nodesource.com/setup_8.x | bash \
 && apt-get install -y apt-utils \
 && apt-get install -y nodejs \
 && mix local.hex --force \
 && mix local.rebar --force \
 && mix archive.install --force https://github.com/phoenixframework/archives/raw/master/phx_new-1.3.4.ez

ENV APP_HOME /app 
RUN mkdir -p /app
WORKDIR $APP_HOME

EXPOSE 4000

CMD ["mix", "phx.server"]
