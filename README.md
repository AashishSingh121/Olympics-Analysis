# Olympics-Analysis
1. In how many cities Summer Olympics is held so far?
  Selecting unique cities from the dataset
  \\sol=pd.DataFrame(df["City"].unique())
  Counting the number of rows in the dataset
  \\count=len(sol.axes[0])
  \\Output:Number Of Cities Summer Olympics is held: 22
  
2. Which sport is having most number of Gold Medals so far? (Top 5)\
    Sport having most number of Gold Medals: Athletics 
    Number of Medals: 1214
    1. Atheletics
    2. Swimming
    3. Fencing
    4. Cycling Track
    5. Cycling Road

3. Which sport is having most number of medals so far? (Top 5)
    Sport having most number of Medals: Athletics 
    Number of Medals: 3638
    1. Atheletics
    2. Swimming
    3. Fencing
    4. Cycling Track
    5. Cycling Road

4. Which player has won most number of medals? (Top 5)
    1 :  PHELPS, Michael 22
    2 :  LATYNINA, Larisa 18
    3 :  MANGIAROTTI, Edoardo 13
    4 :  NURMI, Paavo 12
    5 :  OSBURN, Carl Townsend 11
5. Which player has won most number Gold Medals of medals? (Top 5)
    List Of Top 5 players who have most Gold Medals:
    1 :  PHELPS, Michael 18
    2 :  NURMI, Paavo 9
    3 :  EWRY, Ray 8
    4 :  VAN INNIS, Hubert 6
    5 :  SCHUMANN, Carl 4
6. In which year India won first Gold Medal in Summer Olympics?    
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
    Event most popular in terms of number of players: Aquatics 
    Number of players: 4170
    1.Aquatics
    2.Athletics
    3.Gymnastics
    4.Fencing
    5.Cyclic

8. Which sport is having most female Gold Medalists? (Top 5)
    Sport having most female Gold Medalists: Aquatics 
    Number of players: 589
    1.Aquatics
    2.Archery
    3.Tennis
    4.Skating
    5.Golf
