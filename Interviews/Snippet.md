#### [1] A method to calculate the age


```cs
public class MyClass
{
    public static int CalculerAge(DateTime birthday)
    {
        if(DateTime.Today.Month > birthday.Month && DateTime.Today.Month > birthday.Month && DateTime.Today.Day < birthday.Day)
        {
            throw new Exception("Wrong birth date");
        }
        
        int age = DateTime.Today.Year - birthday.Year;
        
        if(DateTime.Today.Month < birthday.Month && DateTime.Today.Day < birthday.Day)
        {
            age--;
        }
        
        return age;
    }
}
var OlivierBirth = new DateTime(1976,5,7);
var OlivierAge = MyClass.CalculerAge(OlivierBirth);
Console.WriteLine(OlivierAge);

OlivierBirth = new DateTime(1976,1,2);
OlivierAge = MyClass.CalculerAge(OlivierBirth);
Console.WriteLine(OlivierAge);

OlivierBirth = new DateTime(2016,5,7);
OlivierAge = MyClass.CalculerAge(OlivierBirth);
Console.WriteLine(OlivierAge);

//Console:
//39
//40
//Exception : ...

```

#### [2] Factorial & Recursivity

```cs

public static int Factorial(int i)
{
    if(i > 1)
    {
        return i * Func(i-1);
    }
    
    return i;
}

Factorial(5) //120

```

_Beware_ about the stack overflow when you use the recursive methods.
