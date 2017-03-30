using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace BotSavesPrincess
{
    class Program
    {
        private static void displayPathtoPrincess(int n, string[] grid)
        {
            int[] mp = new int[2];
            int[] pp = new int[2];
            for (int i = 0; i < n; i++)
            {
                string temp = grid[i];
                int x = temp.IndexOf("m");
                if (x > -1)
                {
                    mp[0] = x;
                    mp[1] = i;
                }
                x = temp.IndexOf("p");
                if (x > -1)
                {
                    pp[0] = x;
                    pp[1] = i;
                }
            }
            int xf = mp[0] - pp[0];
            int yf = mp[1] - pp[1];
            if (xf > 0)
            {
                while (xf != 0)
                {
                    Console.WriteLine("LEFT");
                    xf = xf - 1;
                }
            }
            else if (xf < 0)
            {
                while (xf != 0)
                {
                    Console.WriteLine("RIGHT");
                    xf = xf + 1;
                }
            }
            if (yf > 0)
            {
                while (yf != 0)
                {
                    Console.WriteLine("UP");
                    yf = yf - 1;
                }
            }
            else if (yf < 0)
            {
                while (yf != 0)
                {
                    Console.WriteLine("DOWN");
                    yf = yf + 1;
                }
            }
        }
        static void Main(string[] args)
        {
            int m;
            m = int.Parse(Console.ReadLine());
            String[] grid = new String[m];
            for (int i = 0; i < m; i++)
            {
                grid[i] = Console.ReadLine();
            }
            displayPathtoPrincess(m, grid);
        }
    }
}
