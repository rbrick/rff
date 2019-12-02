# rff
A repository containing numerous ways of reading lines from a file in various languages




# Java 8
```java
import java.nio.charset.Charset;
import java.nio.file.Files;
import java.nio.file.Paths;

Files.readAllLines(Paths.get("input.txt"),  Charset.defaultCharset()).forEach(
                line -> {
                    System.out.println(line);
                }
      );
```

# Java 7

```java
try (Scanner scanner = new Scanner(new FileReader("input.txt"))) {
    while (scanner.hasNext()) {
          System.out.println(scanner.next());
    }
} catch (IOException e) {
    e.printStackTrace();
}
```
