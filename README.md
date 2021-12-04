using System;

namespace ConsoleApp20
{
    class Admin
    {
        public int Number 
                                {get; set;}
        public DateTime Time 
                                {get; set;}
        public string Name 
                                {get; set;}
        public Admin(int number, DateTime time, string name)
        {
            this.Number = number;
            this.Time = time;
            this.Name = name;
        }
    }

    class Worker : Admin
    {
        public string Ptime 
        {get; set;}

        public Worker(int number, DateTime time, string name, string Ltime) : base(number, time, name)
        {
            Ptime = Ltime;
        }
    }

    class Staff : Admin
    {
        public string Work 
        {get; set;}
        public Staff(int number, DateTime time, string name, string work) : base(number, time, name)
        {
            Work = work;
        }
    }

    class Engineer : Staff
    {
        public string Wh 
        {get; set;}

        public Engineer(int number, DateTime time, string name, string wh, string work) : base(number, time, name, work)
        {
            Wh = wh;
        }
    }

    class v2
    {
        static void Main()
        {
            Engineer final = new Engineer(3, DateTime.Now, "1", "2", "3");
            Console.WriteLine(final.Work);
            Console.ReadLine();

        }
    }
}
