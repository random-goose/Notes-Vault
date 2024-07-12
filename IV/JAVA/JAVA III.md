# Exception Handling
Exception handling in Java is a powerful mechanism to handle the runtime errors so that the normal flow of the application can be maintained

## What is an Exception
Exception is an event that disrupts the normal flow of the program. It is an object which is thrown at runtime.

## What is Exception Handling
It is a mechanism to handle runtime errors such as IOException, SQLException, etc.

## Advantages of Exception Handling
The core advantage of exception handling is to maintain the normal flow of the application. An exception normally disrupts of the application that is why we use exception handling.

Suppose there are 10 statements, and there is an exception thrown at line 5, without exception handling, the whole program handling. If we implement execution handling, we can throw an exception, and continue the execution from statement 6.

## Types of Java Exceptions
- Checked 
- Unchecked
- Errors

### Checked
The classes which directly inherit throwable class except RuntimeException are knows as checked exception. Checked exceptions are checked at compile-time.
- IOException
- SQLException
### Unchecked
The classes which inherit RuntimeException are knows as unchecked exceptions. They are not checked at compile-time, but are checked at runtime.
- ArrayOutOfBoundsException
- NullPointerException
- ArithmeticException

### Error
An error is unrecoverable.
- OurOfMemoryError
- VirtualMachineError
- AssertionError


### Keywords
| Keyword  | Meaning                                                                                                                                                                                                                                          |
| -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| try      | The try keyword is used to specify a block where we should place exception code. The must be followed by catch or finally.                                                                                                                       |
| catch    | This is used to handdle the exception, it must be preceded by a try block                                                                                                                                                                        |
| fianally | It is used to execute code regardless of the outcome of the exception or handling                                                                                                                                                                |
| throw    | It is used to throw an exception                                                                                                                                                                                                                 |
| throws   | It is used to declare exceptions, it doesnt throw an exception. It specifies that there might be an exception that can orrur in this method, it is present in the method signature. <br>`returnType methodName(parameters) throws ExceptionType` |

### Example Code
```Java
public class Bava {
    public static void main(String[] args) {
        int a = 10;
        int b = 0;
        int result = 0;

        try {
            result = a / b;
        } catch (ArithmeticException e) {
            System.out.println(e);
        } finally {
            System.out.println("Execution complete.");
        }

        System.out.println("Result: " + result);
    }
}
```
