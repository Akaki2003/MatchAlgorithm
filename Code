using System;
using System.Collections.Generic;


public class prog
{
    public static void Main()
    {
        int number = int.Parse(Console.ReadLine());
        bricks(number);
    }
    public static void bricks(int digits)
    {
        if (digits>0 && digits<4)
        {
            Console.WriteLine(12 + (digits-1) * 8);
        }
        else if (digits == 4)
        {
            Console.WriteLine(33);
        }
        else if (digits > 4)
        {
            int number = afterFour(digits);
            Console.WriteLine(33 + number);
        }
    }
    public static int afterFour(int number)
    {
        List<int> numblist = new List<int>{8,5};
        List<int> added = new List<int> {5,3};
        int sum = 0;
        int i = 0;
        int counter = 0;
        int eightCheck = 0;
        while (i < number - 4)
        {
            counter++;
            sum+=numblist[i];
            i++;
            if (numblist[i-1] == 8)
            {
                eightCheck++;
                if (eightCheck == 1 && counter == 1)
                {
                    numblist.AddRange(added);
                }
                else if (eightCheck == 1 && counter != 1)
                {
                    added.Add(3);
                    numblist.AddRange(added);
                }
                if (eightCheck == 3)
                {
                    numblist.AddRange(added);
                    eightCheck = 0;
                }
            }
            if (i == numblist.Count)
            {
                i = 0;
            }
            if (counter == number - 4)
            {
                break;
            }
        }
        return sum;
    }
}
