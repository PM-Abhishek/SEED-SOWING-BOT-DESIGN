# **Objectives In order of priority**

***
1. Easy to use
2. Wireless control
3. Seed Storage facility
4. Portable
***
# **Weightage table**

***
|SI.No.|Objective             |Weightage             |
|------|----------------------|----------------------|
|1.    | Easy To Use         |9          |
|2.    | Wireless Control         |8         |
|3.    | Seed storage facility         |6          |
|4.    | Portablity               |5          |
***
# **PUGH Chart**
|Objectives    |Weightage  |Design 1               |Design 2               |Design 3               |Design 4               |
|--------------|-----------|-----------------------|-----------------------|-----------------------|-----------------------|
| Easy to use  |  9         | ++          |+           | Datum          |-       |          
| Wireless control|     8        | 0        |0           |Datum                    |   0 |            
|Seed storage facility|  6            | +  |++           |    Datum                |   ++  |
|Portability   |         5  | -        |--         |   Datum    |   +               |
|+ Score       |         |24   |21   |0   | 17  |
|- Score       |         | 5   |10   |0   | 9  |
| Total        |         | 19  |14   | 0  | 8|
***

***
# **Final design**
![img_20190302_214150](https://user-images.githubusercontent.com/46991362/53720506-f2b50480-3e86-11e9-9145-ad91a04e649e.jpg)

***
## **Justification of PUGH Chart**
|Design   |objectives |score given               |Justification            |
|--------------|-----------|-----------------------|-----------------------|
|1| Easy to use|18|It is easier to put seeds into it| 
|1| Wireless control|0|Same as datum|
|1| Seed Storage facility|6|It has more storage capacity|
|1| Portable|-5|As it uses belt drives it is hard to transport it|
|2| Easy to use|9|Easy maintenance than datum|
|2| Wireless control|0|Same as datum.|
|2| Seed Storage facility|12|Larger capacity|
|2| Portable|-10|Because of large container it is harder to carry around|
|3| Easy to use|0|Datum|
|3| Wireless control|0|Datum|
|3| Seed Storage facility|0|Datum|
|3| Portable|0|Datum|
|4| Easy to use|-9|Tough to use|
|4| Wireless control|0|Same as datum|
|4| Seed Storage facility|12|Larger facility|
|4| Portable|5|Easy to port as it has wheels|


***
# **Clustering of Sub-Systems**
![capture2](https://user-images.githubusercontent.com/46917583/53155003-2029c480-35e2-11e9-8f04-d0446fe8442b.PNG)

***
# **Identified List of Sub-Systems**
1.User intereaction-Akshay S Kulkarni
2.Movement-Abhishek R
3.Tilling-Abhishek P M

***
# **Funtional tree**
![capture1](https://user-images.githubusercontent.com/46917583/53155008-228c1e80-35e2-11e9-8ab4-ae2254d88eec.PNG)
***
# **Component Hierarchy**
![capture3](https://user-images.githubusercontent.com/46917583/53161586-48202480-35f0-11e9-9126-7de6904197c4.PNG)
# **System interaction Table**
|       |        |Subsystem 1             |            |
|--------------|-----------|-----------------------|-----------------------|
|        |Sub-system 2|Sub-system 3|Sub-system 4|
|Energy Interaction| Yes|No|No|
|Material Interaction|No|Yes|Yes|
|Data Interaction|Yes|Yes|No|
|Spatial Interaction|No|No|No|

EXPLANATION:Subsystem 1 and subsystem 2 has not to share energy for user interaction  and moving all the subsystems  



|       |        |Subsystem 2             |            |
|--------------|-----------|-----------------------|-----------------------|
|        |Sub-system 1|Sub-system 3|Sub-system 4|
|Energy Interaction|Yes|No|Yes|
|Material Interaction|No|No|Yes|
|Data Interaction|Yes|Yes|Yes|
|Spatial Interaction|Yes|Yes|Yes|

EXPLANATION:Subsystem 2 and 3 has to share energy for moving and seed sowing all the subsystems are connected



|       |        |Subsystem 3             |            |
|--------------|-----------|-----------------------|-----------------------|
|        |Sub-system 1|Sub-system 2|Sub-system 4|
|Energy Interaction|No|No|No|
|Material Interaction|Yes|No|Yes|
|Data Interaction|No|No|No|
|Spatial Interaction|Yes|Yes|Yes|

EXPLANATION:Subsystem 3 share no energy or data because its independent and continuous.



|       |        |Subsystem 4             |            |
|--------------|-----------|-----------------------|-----------------------|
|        |Sub-system 1|Sub-system 2|Sub-system 3|
|Energy Interaction|No|No|No|
|Material Interaction|No|No|No|
|Data Interaction|No|No|No|
|Spatial Interaction|Yes|Yes|Yes|

EXPLANATION:Subsystem 4 is independent of all system so there is no data and energy interaction.