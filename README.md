# Title
## API Server
###  Create Phoenix Project
create project
```
docker-compose run --rm api mix phx.new . --app project_name --database mysql
```
configure database setting
```elixir:api_server/app/config/dev.exs
- hostname: "localhost",
+ hostname: "database",
```
create database
```
docker-compose run --rm api mix ecto.create
```
run
```
docker-compose run --rm api mix phx.server
```

