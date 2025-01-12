# Simple Chat Application

This is a simple chat application built using Java's networking and multithreading capabilities. The project includes a basic server (`VerySimpleChatServer`) and a graphical client (`SimpleChatClient`) that communicate over a TCP connection.

## Features
- Multiple clients can connect to the chat server and send messages to each other.
- Real-time message broadcasting from the server to all connected clients.
- Simple GUI for the client to send and display chat messages.
- The client uses Java Swing for the GUI and runs on separate threads for networking.

## Project Structure
- **`SimpleChatClient.java`**: This is the client application that provides a graphical interface for sending and receiving messages.
- **`VerySimpleChatServer.java`**: This is the server application that handles client connections, reads incoming messages, and broadcasts them to all clients.

## How It Works

### Server (`VerySimpleChatServer`)
1. The server listens for incoming connections on port `5000`.
2. When a client connects, the server adds the client's output stream to a list of connected clients.
3. The server spawns a new thread for each client, which listens for incoming messages from that client.
4. When a message is received, the server broadcasts the message to all connected clients.

### Client (`SimpleChatClient`)
1. The client connects to the server on `127.0.0.1:5000` (local server).
2. It provides a simple graphical interface where the user can type and send messages.
3. Messages from the user are sent to the server, and messages from other clients are displayed in a scrolling text area.
4. The client runs a separate thread to continuously listen for messages from the server.

## How to Run

### Requirements
- Java Development Kit (JDK 8 or higher)
- IDE or terminal for running the Java files

### Steps

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/simple-chat-app.git
   cd simple-chat-app
