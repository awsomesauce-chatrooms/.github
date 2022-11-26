# ASCR Server & Client
A chatroom client-server application written entierly in
TCP sockets, curses and ruby!

## [Protocol Documentation](profile/protocol.md)


# Requirements
1. Ruby 3.1.x. I reccomend using `rbenv` as your version manager (due to IO::Buffer)
2. The following gems
```
gem install curses
gem install lmdb
```

# Usage
To start the server it's trivial `ruby main.rb`. It'll create two folders created config and database_server. Both of these should probably be dockerized and put into a volume (if you're doing that.)

Starting the client however is slightly harder, you have to use something like `ruby main.rb -h localhost -p 8080`. `h` being host, `p` being port.

# Docker Compose
Use the docker compose file inside of server/docker-compose.yml. Github actions automatically does docker image building.

# Monorepo
This is a monorepo, meaning there's both the server and the client in one repo. This allows me to do funky stuff such as having shared files inside of a folder which both use

# Ideas (this is not a todo)
1. Client in non-interactive mode that spits out something json something like `{type: "authenicated", token: "token"}` and `{type: "message", message: "129358: hi"}`

# Other implementations:
1. Currently none

# Bugs:
1. Currently none
