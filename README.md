# Olympics-Analysis
1. In how many cities Summer Olympics is held so far?
  Selecting unique cities from the dataset
  \\sol=pd.DataFrame(df["City"].unique())
  Counting the number of rows in the dataset
  \\count=len(sol.axes[0])
  \\Output:Number Of Cities Summer Olympics is held: 22
  
2. Which sport is having most number of Gold Medals so far? (Top 5)
gold=df.where(df['Medal']=='Gold')
gold=gold.dropna()
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
df=pd.read_csv("D:\Aashish Folder\Docs\Olympics.csv")
​
gold=df.where(df['Medal']=='Gold')
gold=gold.dropna()
data=[]
for x in gold['Discipline'].unique():
    data.append([x , len(gold[gold['Discipline']  ==x])])
sol=0
index=0
for i in range(len(data)):
    if sol<data[i][1]:
        sol=data[i][1]
        index=i    
print("Sport having most number of Gold Medal:",data[index][0],"\nNumber of Medals:",data[index][1])
Sport having most number of Gold Medal: Athletics 
Number of Medals: 1214
3. Which sport is having most number of medals so far? (Top 5)
df
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
df=pd.read_csv("D:\Aashish Folder\Docs\Olympics.csv")
data=[]
for x in df['Discipline'].unique():
    data.append([x , len(df[df['Discipline']  ==x])])
sol=0
index=0
for i in range(len(data)):
    if sol<data[i][1]:
        sol=data[i][1]
        index=i    
print("Sport having most number of Gold Medal:",data[index][0],"\nNumber of Medals:",data[index][1])
​
Sport having most number of Gold Medal: Athletics 
Number of Medals: 3638
4. Which player has won most number of medals? (Top 5)
data=[]
for x in df['Athlete'].unique():
    data.append([x , len(df[df['Athlete']  ==x])])
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
df=pd.read_csv("D:\Aashish Folder\Docs\Olympics.csv")
​
data=[]
for x in df['Athlete'].unique():
    data.append([x , len(df[df['Athlete']  ==x])])
sol=0
index=0
for i in range(len(data)):
    if sol<data[i][1]:
        sol=data[i][1]
        index=i    
print("Athlete having most number of Medals:",data[index][0],"\nNumber of Medals:",data[index][1])
​
Athlete having most number of Medals: PHELPS, Michael 
Number of Medals: 22
5. Which player has won most number Gold Medals of medals? (Top 5)
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
df=pd.read_csv("D:\Aashish Folder\Docs\Olympics.csv")
​
data=[]
gold=df.where(df['Medal']=='Gold')
gold=gold.dropna()
for x in gold['Athlete'].unique():
    data.append([x , len(gold[gold['Athlete']  ==x])])
​
sol=0
index=0
for i in range(len(data)):
    if sol<data[i][1]:
        sol=data[i][1]
        index=i    
print("Athlete having most number of Gold Medal:",data[index][0],"\nNumber of Medals:",data[index][1])
Athlete having most number of Gold Medal: PHELPS, Michael 
Number of Medals: 18
6. In which year India won first Gold Medal in Summer Olympics?
a_gold.where(df["Year"]==k)
res=res.dropna()
print(res)
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
df=pd.read_csv("D:\Aashish Folder\Docs\Olympics.csv")
data=[]
india=df.where(df["Country"]=='IND')
india=india.dropna()
india_gold=india.where(df["Medal"]=='Gold')
india_gold=india_gold.dropna()
​
y=int(2020)
k=''
for i in india_gold['Year'].unique():
    if int(i)<y:
        y=int(i)
        k=i
print("India won first Gold Medal in Summer Olympics In Year:",y)
print("\n Medal won in",y,":")
res=india_gold.where(df["Year"]==k)
res=res.dropna()
print(res)
    
India won first Gold Medal in Summer Olympics In Year: 1928

 Medal won in 1928 :
        Year       City   Sport Discipline                       Athlete  \
5512  1928.0  Amsterdam  Hockey     Hockey          ALLEN, Richard James   
5513  1928.0  Amsterdam  Hockey     Hockey                   CHAND, Dyan   
5514  1928.0  Amsterdam  Hockey     Hockey           GATELEY, Maurice A.   
5515  1928.0  Amsterdam  Hockey     Hockey                   GILL, K. S.   
5516  1928.0  Amsterdam  Hockey     Hockey  GOODSIR-CULLEN, William John   
5517  1928.0  Amsterdam  Hockey     Hockey       HAMMOND, Leslie Charles   
5518  1928.0  Amsterdam  Hockey     Hockey            KHAN, Feroze Uddin   
5519  1928.0  Amsterdam  Hockey     Hockey           MARTHINS, George E.   
5520  1928.0  Amsterdam  Hockey     Hockey                NORRIS, Rex A.   
5521  1928.0  Amsterdam  Hockey     Hockey         PINNIGER, Broome Eric   
5522  1928.0  Amsterdam  Hockey     Hockey            ROCQUE, Michael E.   
5523  1928.0  Amsterdam  Hockey     Hockey           SEAMAN, Frederic S.   
5524  1928.0  Amsterdam  Hockey     Hockey                  SHAUKAT, Ali   
5525  1928.0  Amsterdam  Hockey     Hockey                 SINGH, Jaipal   
5526  1928.0  Amsterdam  Hockey     Hockey          YUSUF, Sayed Mohamed   

     Country Gender   Event Medal  
5512     IND    Men  Hockey  Gold  
5513     IND    Men  Hockey  Gold  
5514     IND    Men  Hockey  Gold  
5515     IND    Men  Hockey  Gold  
5516     IND    Men  Hockey  Gold  
5517     IND    Men  Hockey  Gold  
5518     IND    Men  Hockey  Gold  
5519     IND    Men  Hockey  Gold  
5520     IND    Men  Hockey  Gold  
5521     IND    Men  Hockey  Gold  
5522     IND    Men  Hockey  Gold  
5523     IND    Men  Hockey  Gold  
5524     IND    Men  Hockey  Gold  
5525     IND    Men  Hockey  Gold  
5526     IND    Men  Hockey  Gold  
7. Which event is most popular in terms on number of players? (Top 5)
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
df=pd.read_csv("D:\Aashish Folder\Docs\Olympics.csv")
data=[]
count=0
for x in df['Sport'].unique():
    data.append([x , len(df[df['Sport']  ==x])])
sorted(data, key = lambda x: x[1])
data1=[]
for i in range(5):
    data1.append(data[i])
for i in range(len(data1)):
    if data1[i][1]>count:
        count=data[i][1]
        index=data[i][0]
pd.DataFrame(data1,columns = ['Sport','freq']).sort_values(by='freq', ascending=False).plot(x = 'Sport', y = 'freq', kind = 'bar', figsize = (10,5))
​
print("Event most popular in terms of number of players:",index,"\nNumber of players:",count)
Event most popular in terms of number of players: Aquatics 
Number of players: 4170

8. Which sport is having most female Gold Medalists? (Top 5)
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
df_1=pd.read_csv("D:\Aashish Folder\Docs\Olympics.csv")
df_2=df_1.where(df_1['Gender']=='Women')
df_2=df_2.dropna()
df=df_2.where(df_2['Medal']=='Gold')
df=df.dropna()
data=[]
count=0
for x in df['Sport'].unique():
    data.append([x , len(df[df['Sport']  ==x])])
sorted(data, key = lambda x: x[1])
data1=[]
for i in range(5):
    data1.append(data[i])
for i in range(len(data1)):
    if data1[i][1]>count:
        count=data[i][1]
        index=data[i][0]
pd.DataFrame(data1,columns = ['Sport','freq']).sort_values(by='freq', ascending=False).plot(x = 'Sport', y = 'freq', kind = 'bar', figsize = (10,5))
​
print("Sport having most female Gold Medalists:",index,"\nNumber of players:",count)
​
Sport having most female Gold Medalists: Aquatics 
Number of players: 589
