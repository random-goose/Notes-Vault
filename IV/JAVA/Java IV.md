# Java Streams
In Java, streams are used to perform I/O Operations. They are primarily categorized into two types: Byte Streams and Character Streams

## Byte Streams
They handle I/O of raw binary data. They read and write data in bytes. Byte streams are typically used for data that is not text, like images or executable files.

### Key Classes:
- FileInputStream
- FileOutputStream
### Example
```Java
import java.io.FileInputStream;
import java.io.FileOutputStream;
import java.io.IOException;

public class ByteStreamExample {
    public static void main(String[] args) {
        FileInputStream fis = null;
        FileOutputStream fos = null;

        try {
            fis = new FileInputStream("inputFile.txt");
            fos = new FileOutputStream("outputFile.txt");
            int byteContent;
            while ((byteContent = fis.read()) != -1) {
                fos.write(byteContent);
            }
            System.out.println("File copied successfully using Byte Streams.");
        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            try {
                if (fis != null) {
                    fis.close();
                }
                if (fos != null) {
                    fos.close();
                }
            } catch (IOException ex) {
                ex.printStackTrace();
            }
        }
    }
}
```

## Character Streams
They handle I/O of character data (text). They read and write in 16-bit Unicode. They are used for text files.

### Key Classes
- FileReader
- FileWriter

### Example
