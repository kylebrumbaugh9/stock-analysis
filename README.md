# VBA of Wall Street

## Overview of Project

### Purpose
The purpose of this analysis was to determine how 12 different green energy stocks performed in the years 2017 and 2018

### Background
Steve recently received his finance degree and wants to analyze green energy stocks to make sure that his parents, his first clients, are investing in an optimal manner. Steve wants to analyze two years worth of trading data for 12 green energy stocks and determine which stocks performed well and which stocks did not so that he can advise his parents. Furthermore, he wants to also ensure that the solution that we build to analyze the data is scalable and efficient.

## Results
### Stock performance analysis

![All_Stocks_2017_results](https://user-images.githubusercontent.com/114685724/199139171-4d42f84d-999e-42e8-8c97-4cc8a579f5a1.jpg)

After analyzing 2017, I found that the majority of green energy stocks were up! Almost every green energy stock, with the exception of TERP, ended the year 2017 at a higher stock price than it started. DQ and SEDG were the two highest performers, garnering returns over 180%!


![All_Stocks_2018_Results](https://user-images.githubusercontent.com/114685724/199139175-8787dfeb-ce23-4fdb-ab2e-d4e45b7957ed.jpg)

2018 was a different story for green energy stocks: almost all stocks were down. Most stocks closed the year worse off than where they started except for ENPH and RUN which were both up over 80%. Those two stocks had posted gains in 2017 as well, albeit RUN's return in 2017 was minimal (5.5%) compared to ENPH's return (129.5%).

### Macro Execution Time analysis

The intial code that I wrote was functional, but I wasn't sure it would be performant at scale. I refactored the code to make the code run more efficiently.

![VBA_Challenge_2017_Original_Code](https://user-images.githubusercontent.com/114685724/199140035-64e089d1-f40a-473d-89a5-095d4adc5edf.jpg)

The 2017 original code ran in 0.54 seconds. After refactoring this code, I was able to get it to run in 0.48 seconds

![VBA_Challenge_2017_Refactored_Code](https://user-images.githubusercontent.com/114685724/199140099-9ea5afec-b31d-407b-942a-bc716dddc730.jpg)

While this may not seem like a lot, it's because it's only looping 12 stocks. If we were to loop this code over 12,000 stocks, our code would run a full minute faster. 


![VBA_Challenge_2018_Original_Code](https://user-images.githubusercontent.com/114685724/199140326-eed24dd7-ccc3-4177-9b24-433186f699b1.jpg)

![VBA_Challenge_2018_Refactored_Code](https://user-images.githubusercontent.com/114685724/199140335-3fb9a2d5-d745-4d39-8841-f4522cd85c98.jpg)

I found very similar results with the 2018 code. The original code ran in 0.56 seconds while the refactored code ran in 0.48 seconds. 

Overall, the refactored code was more performant than the original code. 


##Summary

Overall, refactoring code comes with advantages and disadvantages, in general. A few advantages are that the code runs more efficiently, can be cleaned up, and can scale more effectively. A few disadvantages are that you can create bugs in code that already works, you can overcomplicate, and you could end up wasting time ending up right where you started. Refactoring this code specifically ended up creating a few advantages and a few disadvantages. On the plus side, the code ran more efficiently and still provided accurate data. I was also able to organize the code more effectively and utilize more whitespace. It forced me to rethink the code and talk it out. Even though I used more whitespace to "beautify" it, I used fewer lines of code with the refactored data: 151 lines refactored vs 211 original.  On the other hand, it introduced more complexity and included more loops and advanced logic that required more thought. It was difficult for a newbie like me!
