using System;
using System.Collections;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace DigitalCameraAutodetect_DayOrNight
{
    class Program
    {
        static void Main(string[] args)
        {
            StreamReader sr = new StreamReader("e:\\test\\2d3.txt", Encoding.Default);
            string line;
            string str = "";
            int count = 0;
            double ally = 0.0;
            while ((line = sr.ReadLine()) != null)
            {
                str = str + line + "\n";
            }
            String[] str_array0 = str.Split('\n');
            for (int i = 0; i < str_array0.Length; i++)
            {
                String[] str_array1 = str_array0[i].Split(' ');
                for (int n = 0; n < str_array1.Length; n++)
                {
                    string[] str_array_temp = str_array1[n].Split(',');
                    if (str_array_temp.Length == 3)
                    {
                        int[] int_array_temp = Array.ConvertAll(str_array_temp, Int32.Parse);
                        double[] d_array = new double[3];
                        double r = int_array_temp[0];
                        double g = int_array_temp[1];
                        double b = int_array_temp[2];
                        double y = RGBToY(r, g, b);
                        ally += y;
                        count++;
                    }
                }
            }
            ally = ally / count;
            if (ally < 89)
                Console.WriteLine("night");
            else
                Console.WriteLine("day");
        }
        private static double RGBToY(double r, double g, double b)
        {
            double y = r * 0.299 + g * 0.587 + b * 0.114;
            return y;
        }
    }
}
