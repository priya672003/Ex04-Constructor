# Ex04-Constructor
## Aim:
 To write a C# program to calculate the salary of an employee by passing the name, designation, noofexperience, basic salary and insurance amount through constructor.
 
 ## Algorithm:
 
 
 ### Step1:
 
 
 
 ## Program:
 
 ```python3
 
 using System;
namespace Hello
{
    class Employ
    {
        public string name, designation;
        public int noofexperience, basicsalary , insuranceamount;
        float hra, ta, income;
        public Employ(string name, string designation, int noofexperience, int basicsalary, int insuranceamount)
        {
            this.name = name;
            this.designation = designation;
            this.noofexperience = noofexperience;
            this.basicsalary = basicsalary;
            this.insuranceamount = insuranceamount;
        }
        public void salary()
        {
            hra = (20 / 100) * this.basicsalary;
            ta =(10/100)*this.basicsalary;
            income = hra + ta + this.basicsalary - this.insuranceamount;
        }

        public void display()
        {
            Console.WriteLine("Name of the employee is {0} having {1} of experience, working as {2}",this.name,this.noofexperience,this.designation);
            Console.WriteLine("Receives {0} of salary",income);
        }
        public static void Main(String[] args)
        {
            Employ emp1 = new Employ("Hari", "Tester", 10, 30000, 1000);
            Employ emp2 = new Employ("Latha", "Developer", 5, 25000, 1000);

            emp1.salary();
            emp2.salary();
            emp1.display();
            emp2.display();
            
        }
    }
}

```
 
 ## Output:
 
 
 ![image](https://user-images.githubusercontent.com/81132849/166909041-3df4bc23-2938-4219-bcca-4649cbbfda24.png)

 
 ## Result:
