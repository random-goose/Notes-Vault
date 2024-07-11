## History and Structure of Java
It was invented by James Gosling and his colleagues at Sun Microsystems in the early 1990s. It was originally designed for live television, and was migrated to internet programming and was incorporated into the then most used browser, Netscape Navigator. 

Java is compiled into Byte Code, which is then run by the JVM. It borrows syntax style from c++ using curly braces and code blocks, and it borrows object-oriented programming paradigm from c++. 

**JDK:** Java Development Kit, it is a software development environment used to develop Java applications and applets. It contains JRE, development tools and a private JVM.

**JRE:** Java Runtime Environment. It is an implementation of JVM and provides a runtime environment for Java programs. It is a set of software tools designed to run other software.

**JVM:** Java Virtual Machine is a *platform-independent* abstract machine that is responsible for executing Java programs line by line. It is contained or in-built in both JDK and JRE.

## Data Types
- **byte:** whole number from -127 to 127
- **short:** whole number from -32768 to 32767
- **int:** whole number from -2B to 2B
- **long:** whole number from -9Q to 9Q
- **float:** 32-bit IEEE 754
- **double:** 64-bit IEEE 754
- **Boolean:** true / false
- **char:** single Unicode char
- **String:** sequence of characters in double quotes

## Buzzwords
- **Object-Oriented:** Everything in Java is an object
- **Simple:** Syntax based C, no pointers
- **Secured:**
- **Platform Independent:**
- **Robust:**
- **Portable:**
- **Architecture Neutral:**
- **Dynamic:**
- **Interpreted:**
- **High Performance:**
- **Multithreaded:**
- **Distributed:**

## Type Casting
It is the process of converting a value from one data type to another data type. There are two methods:

- Implicit Type Casting (Automatic Type Conversion)
	This type of conversion happens automatically b the Java compiler when there is no risk of losing information.
	It occurs only when the compiler can safely and implicitly convert a value from one data type to another
```Java
	int a = 5;
	long b = a;
```

- Explicit Type Casting
	also known as type promotion or type conversion, and requires the use of a type conversion operator
	Its used when there is a risk of losing info during the conversion or when you want to treat the value as another data type, even if the conversion is not inherently safe.
	
``` Java
	double pi = 3.14;
	int piInt = (int) pi;
```

When performing explicit casting, if the conversion results in a loss of precision or data, the Java compiler with throw a warning but not an error and continue the compilation.


```java
import java.util.Scanner
public class Main {
	public static void main(String args[]) {
		Scanner S = new Scanner(System.in);
		int x;
		int fact = 1
		x = S.nextInt();
		if ((x%2)==0) {
			System.out.println("Even");
		}
		else {
			System.out.println("Odd")
		}
		for (int i=1; i<=n; i++) {
			fact *= i; 
		}
		System.out.println("Factorial is: " + fact)
	}
}
```

## Garbage Collection
In java, garbage means unreferenced objects. It is a process of reclaiming runtime unused memory automatically. In other words, it is a way to destroy the unused objects.
To do so, we would use the free() function in C, but in java, this is performed automatically. So, we can say that java does a better job at garbage collection. 

Advantages of Garbage Collection:
- It makes Java memory efficient because garbage collection removes the unreferenced objects from the memory heap.
- It is automatically done by the garbage collector (a part of JVM) so we don't need to do any extra efforts.

How can Objects be unreferenced:
- By nulling the reference
- By assigning a reference to another
- By creating an anonymous object

Null Reference:
```Java
Employee e = new Employee();
e = null;
```

Assigning a reference to another:
```Java
Employee e1 = new Employee();
Employee e2 = new Employee();
e1 = e2
```

Anonymous Object:
```Java
new Employee();
```

## String & StringBuilder Class

### String Class
The string class represents immutable character sequences. Once a string object in created, it cannot be changed. Any modifications to a string object creates a new string object.

```Java
public class StringLantidi {
    public static void main(String[] args) {
        String str1 = "Kuthha";
        String str2 = str1 + " Chhekestaaru";

        System.out.println("str1: " + str1);
        System.out.println("str2: " + str2);
    }
}
```

### StringBuilder Class
The StringBuilder class represents mutable sequences of characters. Unlike a String, a StringBuilder can be modified after it is created, which makes it more efficient for scenarios involving numerous string manipulations

```Java
public class StringBuilderLantidi {
    public static void main(String[] args) {
        StringBuilder sb = new StringBuilder("Kuthha");
        sb.append(" Chhekestaaru");

        System.out.println("StringBuilder: " + sb.toString());
    }
}
```

#### Key Differences
|          \        | String                                                    | StringBuilder                                                                  |
| ----------------- | --------------------------------------------------------- | ------------------------------------------------------------------------------ |
| **Mutability**    | Immutable                                                 | Mutable                                                                        |
| **Performance**   | Inefficient for heavy modifications (creates new objects) | Efficient for heavy modifications (modifies in place)                          |
| **Thread Safety** | Thread-safe (immutable)                                   | Not thread-safe (mutable)                                                      |
| **Usage**         | Use when you need a constant, unchanging string           | Use when you need to modify the string frequently and performance is a concern |

