### Polymorphism vs hidding

The purpose of the polymorphism is to redefine the behavior of a instance's methode.  
The hidding method is just to hide the base class behavior.

##### Example

```cs 

public class BaseClass
{
  public [baseClassKeyword] void Method()
  {
    Console.WriteLine("I am the base class");
  }
}


public class InheritedClass : BaseClass
{
  public [inheritedClassKeyword] void Method()
  {
    Console.WriteLine("I am the inherited class");
  }
}
```

And we will replace [baseClassKeyword] and [inheritedClassKeyword] by different combinations using ```abstract```,
```override```, ```virtual```, ```new```.

#### The resume

|:-------------------------------------------------------|:------------------------------|
| Base class                                             | ```public void Method```      |
| Inherited class                                        | ```public override Method()```|
| Compilation                                            | KO                            |
| BaseClass a = new InheritedClass(); <br/>  a.Method(); | I am the inherited class

