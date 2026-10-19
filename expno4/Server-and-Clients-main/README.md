# Java Client-Server Socket Programming

## 📌 Description

This project demonstrates **Client-Server Communication using Socket Programming in Java**.

The server waits for a client connection on **port 5000**. Once the client connects, the client sends a message `"Hello Server"` to the server. The server receives the message and sends `"Hello Client"` as a response.

This project helps in understanding the basic concept of **network communication using Java Sockets**.

## 🛠️ Technologies Used

* Java
* Socket Programming
* `java.net` package
* `java.io` package

## 📂 Project Structure

```text
Client-Server/
│
├── client.java
├── server.java
└── README.md
```

## 🔄 How It Works

### Server

1. Creates a `ServerSocket` on port **5000**.
2. Waits for a client using `accept()`.
3. Receives the message sent by the client.
4. Prints the received message.
5. Sends `"Hello Client"` back to the client.
6. Closes the connection.

### Client

1. Connects to the server using `localhost` and port **5000**.
2. Sends `"Hello Server"` to the server.
3. Receives the server's response.
4. Prints the response.
5. Closes the connection.

## ▶️ How to Run

### Step 1: Compile the programs

Open the terminal in the project folder and run:

```bash
javac server.java
javac client.java
```

### Step 2: Start the Server

Run:

```bash
java server
```

You will see:

```text
Server started...
Waiting for client...
```

### Step 3: Start the Client

Open another terminal in the same folder and run:

```bash
java client
```

## 💻 Expected Output

### Server Output

```text
Server started...
Waiting for client...
Client connected.
Client says: Hello Server
Connection closed.
```

### Client Output

```text
Connected to server.
Server says: Hello Client
Connection closed.
```

## 📚 Concepts Covered

* Client-Server Architecture
* Java Socket Programming
* `ServerSocket`
* `Socket`
* `BufferedReader`
* `PrintWriter`
* Input and Output Streams
* TCP Communication
* Exception Handling

## 🎯 Purpose

The main purpose of this project is to understand how two Java programs can communicate with each other over a network using **TCP sockets**.

## 👩‍💻 Author

Rajat Dwivedi
