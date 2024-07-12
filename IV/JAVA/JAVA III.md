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