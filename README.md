# Client-Server Chat Application

This is a basic client-server chat application written in C using sockets and pthreads. The application allows multiple clients to connect to a server and exchange messages in a chatroom-like environment.

## Files

1. **my_server.c**: The server-side code for accepting client connections, managing the chatroom, and handling communication between clients.

2. **my_client.c**: The client-side code for connecting to the server, sending and receiving messages.

## Compilation

To compile the client and server programs, use the following commands:

```bash
gcc my_client.c -o client -pthread
gcc my_server.c -o server -pthread
```

## Usage

### Server

Run the server by providing the port number as a command-line argument:

```bash
./server <port>
```

The server will listen for incoming connections on the specified port.

### Client

Run the client by providing the server's IP address and port number as command-line arguments:

```bash
./client <port>
```

You will be prompted to enter your name before joining the chatroom. Type "exit" to leave the chatroom.

## Features

- Clients can connect to the server using a specified port.
- Clients can send and receive messages in a chatroom environment.
- The server handles multiple clients concurrently using pthreads.
- Graceful handling of client disconnections.

## Notes

- The server has a maximum limit of clients (MAX_CLIENTS) to prevent overloading.
- The client-server communication is basic, and the application does not handle advanced features such as authentication or encryption.

Feel free to modify and enhance the code to suit your specific requirements!
