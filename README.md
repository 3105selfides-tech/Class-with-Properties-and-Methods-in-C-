using System;

namespace StudentClassDemo
{
    // Student class definition
    class Student
    {
        // Properties
        public string Name { get; set; }
        public int Age { get; set; }
        public double Grade { get; set; }

        // Method to display student information
        public void DisplayInfo()
        {
            Console.WriteLine("Student Information:");
            Console.WriteLine($"Name  : {Name}");
            Console.WriteLine($"Age   : {Age}");
            Console.WriteLine($"Grade : {Grade}");
        }

        // Method to check if student passed
        public bool IsPassed()
        {
            return Grade >= 75;
        }
    }

    class Program
    {
        static void Main(string[] args)
        {
            // Create an instance of the Student class
            Student student = new Student();

            // Assign sample values
            student.Name = "Aria";
            student.Age = 20;
            student.Grade = 90;

            // Call methods
            student.DisplayInfo();

            // Display pass/fail result
            if (student.IsPassed())
            {
                Console.WriteLine("Status: Passed");
            }
            else
            {
                Console.WriteLine("Status: Failed");
            }

            Console.ReadLine(); // Keep console window open
        }
    }
}
