## Technical

1. How to use I/O stream to read from a file in Java? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

To use I/O stream to read from a file in Java, you can follow these steps:

- Create a File object that represents the file you want to read.
- Create a FileInputStream object by passing the File object to its constructor.
- Create a BufferedInputStream object by passing the FileInputStream object to its constructor.
- Create a byte array with a suitable size to store the contents of the file.
- Use the read() method of the BufferedInputStream object to read the contents of the file into the byte array.
- Close the BufferedInputStream object and the FileInputStream object.

Here's an example code snippet that demonstrates how to read the contents of a file using I/O stream:

```Java
File file = new File("example.txt");
FileInputStream fis = new FileInputStream(file);
BufferedInputStream bis = new BufferedInputStream(fis);
byte[] buffer = new byte[1024];
int bytesRead = 0;
while ((bytesRead = bis.read(buffer)) != -1) {
    // process the contents of the buffer
}
bis.close();
fis.close();
```

</blockquote>

</details>

---

2. Can you tell us about the bufferReader and fileReader in Java? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

In Java, BufferedReader and FileReader are commonly used for reading files. FileReader is used to read character files, while BufferedReader is used to read larger files more efficiently by buffering the input.

*FileReader*: This class reads a file one character at a time. It is a subclass of InputStreamReader, which reads bytes and converts them into characters using a specified character encoding. FileReader is easy to use, but it is not very efficient when reading large files.

*BufferedReader*: This class reads a file line by line, using a buffer to improve performance. It reads a chunk of characters from the file into a buffer and then returns one line at a time. BufferedReader is more efficient than FileReader for reading large files.

</blockquote>

</details>

---

3. Can you brief on Serialization in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Serialization in Java is the process of converting an object into a byte stream that can be persisted into a file, transferred over a network, or stored in a database. Deserialization is the reverse process of converting the byte stream back into an object.

The Serializable interface is used to mark a class as serializable, and the ObjectOutputStream and ObjectInputStream classes are used for serialization and deserialization respectively. During serialization, all non-transient fields of the object are written to the byte stream, which can then be used to reconstruct the object during deserialization.

</blockquote>

</details>

---

4. How can I write to a file in Java?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

You can write to a file in Java using classes like FileOutputStream, BufferedWriter, or PrintWriter. Here's an example using BufferedWriter:

```java
try (BufferedWriter writer = new BufferedWriter(new FileWriter("file.txt"))) {
    writer.write("Hello, World!");
} catch (IOException e) {
    e.printStackTrace();
}
```

</blockquote>

</details>

---

5. How can I create a directory in Java?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

You can create a directory in Java using the mkdir() or mkdirs() methods of the File class. The mkdir() method creates a single directory, while mkdirs() creates multiple directories recursively if needed. Here's an example:

```java
File directory = new File("mydir");
if (directory.mkdir()) {
    System.out.println("Directory created successfully.");
} else {
    System.out.println("Failed to create directory.");
}
```

</blockquote>

</details>

---

6. How can I delete a file in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

You can delete a file in Java using the delete() method of the File class. Here's an example:

```java
File file = new File("file.txt");
if (file.delete()) {
    System.out.println("File deleted successfully.");
} else {
    System.out.println("Failed to delete file.");
}
```
</blockquote>

</details>

---