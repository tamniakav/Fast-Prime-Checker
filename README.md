# Fast-Prime-Checker
Just another repository
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Fast_Prime_Checker___Refactor
{
    class Program
    {
        static void Main(string[] args)
        {
            int num = int.Parse(Console.ReadLine());

            for (int i = 2; i <= num; i++)
            {
                bool isPrimeNumber = true;

                for (int j = 2; j <= Math.Sqrt(i); j++)
                {
                    if (i % j == 0)
                    {
                        isPrimeNumber = false;
                        break;
                    }
                }

                Console.WriteLine($"{i} -> {isPrimeNumber}");
            }
        }
    }
}
