# Delegate
- **What is delegate?**

*1. A bit like an interface with single method. (Signature of a method/ a pointer to a function)*
*2. Hold a reference to a method and the target object the method should be called on*





Any delegate type you create has the members inherited from its parent types, one constructor with parameters of object and IntPtr and three extra methods: Invoke, BeginInvoke and EndInvoke. We'll come back to the constructor in a minute. The methods can't be inherited from anything, because the signatures vary according to the signature the delegate is declared with. Using the sample code above, the first delegate has the following methods:


```java
class Program
{
    // declare delegate
    public delegate void Print(int value);

    static void Main(string[] args)
    {
        // Print delegate points to PrintNumber
        Print printDel = PrintNumber;
          
        printDel(100000);
        printDel(200);

        // Print delegate points to PrintMoney
        printDel = PrintMoney;

        printDel(10000);
        printDel(200);
    }

    public static void PrintNumber(int num)
    {
        Console.WriteLine("Number: {0,-12:N0}",num);
    }

    public static void PrintMoney(int money)
    {
        Console.WriteLine("Money: {0:C}", money);
    }
}
```


- **Why/When to use delegate?**







# Event

- **What is Events?**
 
*1. Something special that is going to happen*
*2. An event has a `publisher`, `subscriber`, `notification` and a `handler`.*



- **Why/When to use events?**


