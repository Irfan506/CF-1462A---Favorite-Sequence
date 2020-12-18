# CF-1462A---Favorite-Sequence
using System;

namespace string_generation
{
    class Program
    {
        static void Main(string[] args)
        {
            int t = Convert.ToInt32(Console.ReadLine());
            while(t>0)
            {
                t--;
                int n = Convert.ToInt32(Console.ReadLine());
                int[] arr = new int[n + 1];
                string[] sp = Console.ReadLine().Split(' ');
                for (int i = 1; i <= n; i++)
                {
                    arr[i] = int.Parse(sp[i-1]);

                }
                for (int i = 1, k = 1, j = n, flag = 0; i <= n; i++)
                {
                    if (flag == 0)
                    {
                        Console.Write(arr[k]);
                        Console.Write(' ');
                        flag = 1;
                        k++;
                    }
                    else
                    {
                        Console.Write(arr[j]);
                        Console.Write(' ');
                        flag = 0;
                        j--;
                    }
                }
                Console.WriteLine();
            }
        }
    }
}
