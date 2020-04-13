# Working With Data

### Serialization & Persistence

* Text
* XML
* JSON

### Data Modeling

* Conceptual, Logical, and Physical Modeling

### Data and Code

* Data Access Object \(DAO\) Pattern
* Object-Relational Management \(ORM\) Guidance

### RDBMS and NoSQL

* Examine use cases for each
* Revisit physical data modeling for NoSQL

### Persistence

* Make data available in the future
  * Save data to non-volatile storage \(i.e., storage that survives a "restart"\)

### Serialization

* Serializing involves converting in-memory objects into data so that it can be:
  * Written/saved somewhere
  * Streamed across a communication link
  * In this context, data means a string or an array of bytes
* Deserialize
  * Convert \(serialized\) data into in-memory objects

### Serialization vs. Persistence

* We persist serialized objects
* We deserialize data read from persistent storage

```text
LocalDateTime t = LocalDateTime.now();
System.out.println("serializing " + t);

OutputStream out = new FileOutputStream(new File("tmp.data"));
ObjectOutputStream serializer = new ObjectOutputStream(out);
serializer.writeObject(t);
out.close();

InputStream in = new FileInputStream(new File("tmp.data"));
ObjectInputStream deserializer = new ObjectInputStream(in);
LocalDateTime t2 = (localDateTime) deserializer.readObject();
System.out.println("Deserialized " + t2);
in.close();
```

### Built-In Serialization Limitations

* Cannot serialize arbitrary objects
  * Objects must implement java.io.Serializable
  * The transitive closure \(i.e., objects, their references, their references' references, and so on\) must implement Serializable as well
* Deserialization is messy
  * Requires casting
  * Requires us to know what type of object we are reading
* Not cross-language
  * Uses a java-specific binary format
* Instances can be serialized, but not the classes themselves
  * Therefore, cannot deserialize data without the compiled classes
* Not ideal
  * E.g. images can be serialized using more suitable formats, such as png, jpg, svg, etc.

### Serialize To Text

* How can we overcome the limitations of Java's built-in serialization?
  * One option is to serialize objects to text
    * Flexibility - easily define custom serialization
    * Convenient deserialization - read text, then determine the type of the object
    * Cross-language - every programming language is capable of text processing
    * Convenient debugging - text is human-readable

