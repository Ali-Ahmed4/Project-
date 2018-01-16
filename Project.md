# Project-
Suffix Array 

    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;
    using System.IO;




     namespace Project_Suffix
    {

        class Program
    {
    
        static void Main(string[] args)
        {
        
        
            StreamReader sr = new StreamReader("C:\\Sample.txt");
            
            //Read the first line of text
        //    string s1 = sr.ReadLine();
            string s1 = "Banana";
            int s = s1.Length;
            
            int i = 0;
            
            int e=0;
            string[] s2 = new string[s+1];
            

            for (i = 0; i <= s;i++ )
            {

                s2[e] = s1.Substring(Math.Max(0, s1.Length - i));
                e++;
            }

            for (i = 0; i <= s;i++ )
            {
                Console.WriteLine(s2[i]);
            }

            Array.Sort(s2, StringComparer.InvariantCulture); 

            for (i = 0; i <= s; i++)
            {
                Console.WriteLine(s2[i]);
            }



                Console.ReadLine();
           } 
        }
    }
