# oop_assign1
implementing inheritance and encapsulation without abstraction and polymorphism

using System;

 class Car
{   //Adding Encapsulation from attributes of a Car
    public string Model { get; protected set; }
    public string Make { get; protected set; }
    public int Year { get; protected set; }
    
    //Attributes
   // public string Model;
   // public string Make;
   // public int Year;

    //Constructor
    public Car(string model, string make, int year)
    {
        Model = model;
        Make = make;
        Year = year;
    }

    //Methods
    public void Drive()
    {
        Console.WriteLine("The car is now running.");
    }

    public void Stop()
    {
        Console.WriteLine("The car has stopped.");
    }
}

    //Adding Inheritance from Car Class
class Bus : Car
{   //Adding Encapsulation from attributes of Bus
    public string Engine { get; protected set; }
    public string Type { get; protected set; }

    //Attributes
   // public string Engine;
   // public string Type;

    //Constructor
    public Bus(string engine, string type, string model, string make, int year)
        : base(model, make, year)
    {
        Engine = engine;
        Type = type;
    }

    //Methods
    public void Accelerate()
    {
        Console.WriteLine("The Bus is now accelerating");
    }

}

class Program
{
    static void Main(string[] args)
    {
        Car myCar = new Car("Toyota", "Corolla", 2023);
        Console.WriteLine($"Model: {myCar.Model}, Make: {myCar.Make}, Year: {myCar.Year}");
        myCar.Drive();
        myCar.Stop();

        Bus myBus = new Bus("YC6K Series Gas Engine", "Shuttle Bus", "BGC Bus", "Victory Liner", 2050 );
        Console.WriteLine($"Engine: {myBus.Engine}, Type: {myBus.Type}");
        myBus.Drive();
        myBus.Stop();
        myBus.Accelerate();
    }
}

