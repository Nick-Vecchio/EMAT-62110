This folder in the EMAT repo is to keep track of all files related to the final project as well as milestone notes.

Milestone 1

For Milestone 1, I set the goal of having collected and tidy the data needed for this project. I have a tidy data set already imported into my notebook. However, the inflation data is a little trickier to work with. I am having to learn some terminology to understand if the data I have found is what I am actually looking for. The two main sources I am looking at inflation data are the World Bank and the Federal Reserve Bank.

As mentioned in the notebook, I found a great dataset but then wanted to make sure that it was accurate, real-world, non-proprietary data. After tracking down the original sources I believe them to be credible and that the combined dataset represents the information accurately enough for our purposes. 

I am a history buff and so know the dates of many conflicts and world events. Though I do believe that I can find this information from a credible source. The question is can I find a miracle and someone has taken world events and conflicts and put them in a csv file with the date and name. Then I can use that to map certain events on the visuals.

Data Sources:
Combined Dataset: 
https://datahub.io/core/gold-prices#notes-from-the-sources

Past Dataset (National Mining Association): https://nma.org/wp-content/uploads/2023/02/his_gold_prices_1833_pres_2023.pdf

Recent Dataset (World Gold Council): https://www.gold.org/download/file/8369/Prices.xlsx


Milestone 2

For Milestone 2, I set the goal of having initial visualizations created. I admit that I am a bit behind in this goal. I struggled immensely with converting the inflation data into a similar format to the gold price data. I was having many issues figuring out why my melt function was not working correctly. I basically was taking the wide inflation data and turning it into long data. To do this, I had to take the heaader row of each column for the month and then create a key value to the numeric dates used in the gold price data. So, Jan = 01, Feb = 02, etc. Then I had to account for the years as well and take those values and concatenate them into something like 1958-01. By doing this I can now have both data sets in the same visualization. Additionally, I dropped a couple of columns in the inflation data prior to importing that were not relevant. 
The trouble I was having with the melt is that it was only seemingly capturing the first month of the year. Through a whole bunch of debugging (print statements) and also exporting my data frame I determined that the data frame was indeed coming over as expected however I ahd to use a sort by date on it.

The inflation data was taken from the Bureau of Labor Statistics website. This is data that I believe is reliable (however I would never bet a million dollars on any data lol). https://data.bls.gov/pdq/SurveyOutputServlet This may not take you to the data I downloaded. To get there, I used these parameters:
Change Output Options:	From: 1957    To: 2024
 	 include graphs checked  include annual averages not checked

Consumer Price Index for All Urban Consumers (CPI-U)

12-Month Percent Change
Series Id:
Not Seasonally Adjusted
Series Title:	All items less food and energy in U.S. city average, all urban consumers, not seasonally adjusted
Area:	U.S. city average
Item:	All items less food and energy
Base Period:	1982-84=100
