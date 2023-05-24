## Technical

1. Differentiate client-side coding and server-side coding.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>


Client-side and server-side coding refer to the location where the code is executed.

Client-side coding is executed on the user's computer, usually in a web browser. Client-side code includes HTML, CSS, and JavaScript. This code is used to build user interfaces, handle user interactions, and perform simple client-side operations, such as form validation.

Server-side coding is executed on the server-side, which is usually a web server. Server-side code includes programming languages like Java, Python, Ruby, and PHP. This code is used to handle complex operations, such as processing data, connecting to databases, and handling user authentication.

</blockquote>

</details>

---

2. Provide an example of client-side bug and server-side bug.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

A client-side bug may include issues related to user input validation, page rendering, or browser compatibility, while a server-side bug may include issues related to database interaction, server configuration, or application logic. Examples of client-side bugs include unhandled user input or unsupported browser versions, while examples of server-side bugs may include incorrect database queries, server crashes, or security vulnerabilities.

</blockquote>

</details>

---

3. What is networking in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Networking in Java refers to the ability of a Java program to communicate over a network, allowing it to send and receive data between different computers or devices.

</blockquote>
</details>

---

4. What are the key classes involved in Java networking?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The key classes involved in Java networking are `Socket`, `ServerSocket`, `InetAddress`, and `URL`.

</blockquote>
</details>

---

5. How do you create a client socket in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

To create a client socket in Java, you can use the `Socket` class. Here's an example:

```java
String serverAddress = "127.0.0.1"; // IP address of the server
int serverPort = 8080; // Port number of the server

try {
    Socket socket = new Socket(serverAddress, serverPort);
    // Now you can use the socket for communication with the server
} catch (IOException e) {
    e.printStackTrace();
}
```
</blockquote>
</details>

---

6. How do you create a server socket in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

To create a server socket in Java, you can use the `ServerSocket` class. Here's an example:

```java
int serverPort = 8080; // Port number to listen on

try {
    ServerSocket serverSocket = new ServerSocket(serverPort);
    // Now the server socket is listening for incoming client connections

    Socket clientSocket = serverSocket.accept();
    // A client connection has been accepted, and you can use the clientSocket for communication with the client
} catch (IOException e) {
    e.printStackTrace();
}
```
</blockquote>
</details>

---

7. How do you read data from a socket in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

You can read data from a socket in Java using an `InputStream`. Here's an example:

```java
try {
    InputStream inputStream = socket.getInputStream();
    InputStreamReader inputStreamReader = new InputStreamReader(inputStream);
    BufferedReader bufferedReader = new BufferedReader(inputStreamReader);

    String data = bufferedReader.readLine();
    // Now you have read a line of data from the socket
} catch (IOException e) {
    e.printStackTrace();
}
```

</blockquote>
</details>

---

8. How do you write data to a socket in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

You can write data to a socket in Java using an `OutputStream`. Here's an example:

```java
try {
    OutputStream outputStream = socket.getOutputStream();
    OutputStreamWriter outputStreamWriter = new OutputStreamWriter(outputStream);
    BufferedWriter bufferedWriter = new BufferedWriter(outputStreamWriter);

    String data = "Hello, server!";
    bufferedWriter.write(data);
    bufferedWriter.newLine();
    bufferedWriter.flush();
    // Now the data has been written to the socket
} catch (IOException e) {
    e.printStackTrace();
}
```

</blockquote>
</details>

---

9.  What is the difference between TCP and UDP in networking?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

TCP (Transmission Control Protocol) is a connection-oriented protocol that provides reliable, ordered, and error-checked delivery of data packets over a network. UDP (User Datagram Protocol), on the other hand, is a connectionless protocol that provides fast and lightweight transmission of data packets but does not guarantee their delivery or order.

</blockquote>
</details>

---

10. How do you handle multiple clients in a server application?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

To handle multiple clients in a server application, you can use multithreading. Each client connection can be handled in a separate thread, allowing the server to handle multiple clients concurrently. You can create a new thread for each accepted client connection and perform the necessary communication and processing within that thread.

</blockquote>
</details>

---

11. How can you implement secure communication using Java networking?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Java provides the Java Secure Socket Extension (JSSE) for implementing secure communication using protocols like SSL/TLS. You can use classes such as `SSLSocket` and `SSLServerSocket` to establish a secure connection. Additionally, you can use certificates for authentication and encryption to ensure secure communication.

</blockquote>
</details>

---

12. What is serialization in Java networking?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Serialization is the process of converting an object into a byte stream so that it can be transmitted over the network or stored in a file. In the context of Java networking, serialization allows objects to be sent as data between the client and server. The `java.io.Serializable` interface is implemented by classes that need to be serialized, and the `ObjectOutputStream` and `ObjectInputStream` classes are used for serialization and deserialization, respectively.

</blockquote>
</details>

---

13. How can you handle timeouts in Java networking?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

To handle timeouts in Java networking, you can set a timeout value on sockets using the `setSoTimeout()` method. This method sets the maximum time a socket will block for input operations. If the timeout expires before data is received, a `SocketTimeoutException` is thrown. You can catch this exception and handle the timeout condition accordingly.

</blockquote>
</details>

---

14. How do you perform asynchronous communication in Java networking?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Asynchronous communication in Java networking can be achieved using non-blocking I/O (NIO). The `java.nio` package provides classes like `Selector`, `Channel`, and `ByteBuffer` that allow for asynchronous I/O operations. By using a selector, you can monitor multiple channels for events and perform I/O operations on them in a non-blocking manner.

These advanced questions delve into topics like protocols, security, concurrency, serialization, and asynchronous communication in Java networking. Understanding these concepts will help you build more robust and efficient networked applications.

</blockquote>
</details>

---