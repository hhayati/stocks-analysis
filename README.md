# stocks-analysis
## Overview of Project
The purpose of this analysis is to provide investing advice based on the trade data of a selected group of 12 individual stocks. The data include opening price, closing price, the high, the low and the total trade volume for each day in 2017 and 2018.  For stock prices, we will only work with closing price for any given day. For this purpose, we will examine the total trade volume and the annual return on each stock. 



## Performance parameters
To evaluate the performance of each stock two variables are calculated. The yearly volume of each stock is calculated by summing up all of the daily volumes. The return for a given stock for a given year is defined as: 

![](https://latex.codecogs.com/gif.latex?%5Csmall%20Stock%20%5C%20Annual%20%5C%20Return%20%3D%5Cleft%20%5B%20%5Cfrac%7BStock%5C%20price%5C%20on%5C%20close%5C%20of%5C%20the%5C%20last%5C%20day%7D%7BStock%5C%20price%5C%20on%5C%20close%5C%20of%5C%20the%5C%20first%5C%20day%7D%20%5Cright%20%5D-1)



## Analysis Results
The VBA macro provides the total stock trade volume and the return for selected stocks in tabular format as shown below. The macro runs after the user inputs the desired year for analysis.  The macro also formats the tabulated data as shown in the Figures. Negative returns (loss) are colored in red while the positive returns (gains)  are colored in green.  

In general, the performance of selected group of the stocks was better in 2017 than in 2018. The median stock return in 2017 was 41.5% while in 2018 the median stock had a loss of 12%.  While 11 out of 12 selected stocks had positive returns in 2017, only 2 out of 12 selected stocks had positive returns in 2018. Notable that 4 of 12 stocks had returns exceeding 100% in 2017.  Also notable are two stocks including ENPH and RUN with positive return in both years.  The total daily volume is highest for FSLR and TERP indicating the stock price is evaluated more accurately compared to stocks with lower trade volumes. 
	

![image](https://user-images.githubusercontent.com/58461542/163526883-fcaffb70-6abd-43f2-b925-49273ebf702c.png)

Figure 1: Stocks performance and volume for years 2017 and 2018



## Refactored Macro Performance
The original VBA macro developed during the study of the course processes selected stocks consecutively, that is,  for each stock loops through the entire rows of the data. The refactored version is tailored for more optimized computational effort by going through the data rows only once. This results in shorter computing time as shown in figure below.



![image](https://user-images.githubusercontent.com/58461542/163527198-8d5bf3f3-ef43-4a84-b95f-cc3ada00e39c.png)




	 	

	


	







Figure 2: Processing times for Refactored code


![image](https://user-images.githubusercontent.com/58461542/163527454-f0a89a0b-2508-446c-921f-8e5a25031416.png)



















Figure 3: Processing times for original code




## Summary

### Advantage of refactored code
In summary, the refactored code runs faster and reduces the computational efforts. The code is more elegant and more efficient.

### Disadvantage of refactored code
In my experience, refactoring the code makes is more complicated and may create errors, so I had to spend a good amount of time to debug. The complicated structure makes it more difficult to track the errors. 
### Final Conclusion
The refactored code is advantageous when the dataset is huge, so the saved processing time is significant. For case of the data used for this challenge, the processing time for original code was still a fraction of a second, so the refactored code while impressively reduced the processing time, it did not provide a practical advantage considering the time spent for debugging.

