问题描述：

C#_linq用法

问题解答：

>  List<TK> tKs = new List<TK>() {
                new TK(){ Name="k1",Key=10,Page=1},
                new TK(){ Name="k2",Key=20,Page=1},
                new TK(){ Name="pk3p",Key=30,Page=2},
                new TK(){ Name="k4",Key=40,Page=2},
                new TK(){ Name="k5",Key=50,Page=1}
                };



> var result = from r in tKs
             orderby r.Key descending
             group r by r.Page into n
             select new
             {
                    n.Key,  //这个Key是Page
                    name = n.First().Name,
                    MaxKey = n.Max(r => r.Key)
              };