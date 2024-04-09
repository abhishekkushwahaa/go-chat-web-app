# Chat Web Application with Golang

This is a simple chat web application using Golang. It uses WebSocket to communicate between clients and server.

## How to run

1. Clone this repository
2. Run the server
   ```bash
   go run server.go
   ```
3. Open the browser and go to `http://localhost:8080`
4. Start chatting!
5. To stop the server, press `Ctrl + C`
6. To run the server again, repeat step 2
7. To run the server in the background, use `nohup`
   ```bash
   nohup go run server.go &
   ```
8. To stop the server running in the background, use `kill`
   ```bash
   kill <PID>
   ```
   where `<PID>` is the process ID of the server

## How it works

1. We create a room with a unique ID when the server starts
2. Clients can join the room by connecting to the server
3. Clients can send messages to the server
4. The server broadcasts the message to all clients in the room
5. Clients can leave the room by disconnecting from the server
6. The server removes the client from the room
7. If there are no clients in the room, the server deletes the room
8. The server can handle multiple rooms at the same time
9. The server can handle multiple clients in the same room

## Technologies used

- Golang
- WebSocket
- HTML & CSS
- Docker
- PostgreSQL

## Features

- [x] Authenticate a user
- [x] Create a user
- [x] Create a room
- [x] Join a room
- [x] Send a message
- [x] Receive a message
- [x] Leave a room
- [x] Delete a room

## Future improvements

- [ ] Add more features
- [ ] Add more tests
- [ ] Add more comments
- [ ] Add more error handling
- [ ] Add more logging
- [ ] Add more security

## Suggestions and feedback

If you have any suggestions or feedback, please create an issue or pull request. Thank you!
