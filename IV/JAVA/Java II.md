## Types of Inheritance in Java

Single
```mermaid
graph TD
	A[Parent Class] --> B[Child Class]
```

Multilevel
```mermaid
graph TD
	A[Parent Class] --> B[Intermediate Class]
	B --> C[Child Class]
```

Hierarchical
```mermaid
graph TD
	A[Parent Class] --> B[Child Class]
	A --> C[Child Class]
```


## Member Access Rulers
They are also called Access Specifiers, they determine the visibility and accessibility of class members (Fields, Methods, Constructions, and Nested Classes) 

- Public
	members are accessible by any other class
	```Java
	public class MyClass {
	    public int publicField;
	    public void publicMethod() { }
	}
```

- Protected
	Members are accessible withing the same package and subclasses, even if they are in different places
```Java
	public class MyClass {
	    protected int protectedField;
	    protected void protectedMethod() { }
	}
```

- Default
	members are only accessible within the same package, this is called `package-private` access
	```Java
	public class MyClass {
	    int defaultField; // No access modifier
	    void defaultMethod() { } // No access modifier
	}
```

- Private
	Members are accessible only within the class where they are defined in

```Java
	public class MyClass {
	    private int privateField;
	    private void privateMethod() { }
	}
```


## Super Keyword
The super keyword in Java is a reference variable which is used to refer immediate parent class object.
Whenever you create the instance of subclass, an instance of parent class is created implicitly which is referred by super reference variable.

Use of Super keyword:
- Super can be used to refer immediate parent class instance variable
- super can be used to invoke immediate parent class method
- super can be used to invoke immediate parent class constructor

``` Java
class Person
{
int id;
String name;
Person(int id, String name)
{
this.id = id;
this.name = name;
}
}
class Emp extends Person
{
float salary;
Emp(int id, String name, float salary)
{
Java Programming CSE
D. JagadeeshBVRIT
super(id, name);//reusing parent constructor
this.salary = salary;
}
void display(){System.out.println(id+" "+name+" "+salary);}
}
class TestSuper
{
public static void main(String[] args)
{
Emp e1 = new Emp(1, "ankit", 45000f);
e1.display();
}
}
```

