# chapter4-exercise9
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Lottery
{
    class Program
    {
        static void Main(string[] args)
        {
            Random random = new Random();
            Random random1 = new Random();
            Random random2 = new Random();
            int num = random.Next(1, 4);
            int num1 = random1.Next(1, 4);
            int num2 = random2.Next(1, 4);
            System.Console.WriteLine("Choose Three Numbers");
            System.Console.WriteLine("Number 1: ");
            string userInput1 = System.Console.ReadLine();
            System.Console.WriteLine("Number 2: ");
            string userInput2 = System.Console.ReadLine();
            System.Console.WriteLine("Number 3: ");
            string userInput3 = System.Console.ReadLine();
            int userNum1 = Convert.ToInt32(userInput1);
            int userNum2 = Convert.ToInt32(userInput2);
            int userNum3 = Convert.ToInt32(userInput3);
            if (num == userNum1 && num1 == userNum2 && num2 == userNum2)
            {
                System.Console.WriteLine("Congratulations you have won $10,000.");
            }
            else if (num == userNum2 && num1 == userNum3 && num2 == userNum1 || num == userNum3 && num1 == userNum1 && num2 == userNum2)
            {
                System.Console.WriteLine("Congratulations you have won $1,000");
            }
            else if (num == userNum1 && num1 == userNum2 || num == userNum1 && num2 == userNum3 || num1 == userNum2 && num2 == userNum3 ||
                num == userNum2 && num1 == userNum3 || num1 == userNum3 && num2 == userNum1 || num == userNum3 && num1 == userNum1 ||
                num == userNum3 && num2 == userNum1 || num1 == userNum3 && num2 == userNum1 || num1 == userNum3 && num2 == userNum2)
            {
                System.Console.WriteLine("Congratulations you have won $100.");
            }
            else if (num == userNum1 || num == userNum2 || num == userNum3 || num1 == userNum1 || num1 == userNum2 || num1 == userNum3 ||
                num2 == userNum1 || num2 == userNum2 || num2 == userNum3)
            {
                System.Console.WriteLine("Congratulations you have won $10.");
            }
            else
            {
                System.Console.WriteLine("Sorry you didn't match any numbers!");
            }
        }
    }
}
