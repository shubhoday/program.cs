# program.cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace dayFinder
{
    class Program
    {
        static void Main(string[] args)
        {
            int day, month, year;
            Console.WriteLine("Enter date 1 (day-month-year) : ");
            string str =Console.ReadLine();
            string[] splitStrArray = str.Split('-');
            day =Convert.ToInt16(splitStrArray[0]);
            month = Convert.ToInt16(splitStrArray[1]);
            year = Convert.ToInt16(splitStrArray[2]);
            uDate date1 = new uDate(day,month,year);

            Console.WriteLine("Enter date 2 (day-month-year) : ");
            str = Console.ReadLine();
            splitStrArray = str.Split('-');
            day = Convert.ToInt16(splitStrArray[0]);
            month = Convert.ToInt16(splitStrArray[1]);
            year = Convert.ToInt16(splitStrArray[2]);
            uDate date2 = new uDate(day, month, year);

            DateFunction obj = new DateFunction();
            int days = obj.getDays(date1,date2);
            Console.WriteLine("the total days : ");
            Console.WriteLine(days);
            Console.ReadKey();
        }
    }
}
