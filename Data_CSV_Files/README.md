# **Data_CSV_Files**
# **Description of Folder - Table of Contents**
## **Unemployment_Monthly.csv**<br>
When looking for data regarding the unemployment rate, I obtained a .csv file from the Federal Reserve Bank of St. Louis ([Federal Reserve Bank of St. Louis, Unemployment Rate, 2025](https://fred.stlouisfed.org/series/UNRATE)). This website provided a graph and a file regarding the unemployment rates from the U.S. Bureau of Labor Statistics. I downloaded the .csv file attached to the website. The file contained the monthly unemployment rates from January 1948 to February 2025; there is an “observation_date” column and an “UNRATE” column. I renamed the columns to “Date” and “Unemployment_Rate.” I shifted all the dates from the first to the last day of the month and converted them to a datetime data type to match all my other data and properly integrate it. The “Unemployment_Rate” column was already a float data type.

## **SP500_data.csv**
I utilized the Yahoo Finance API to find the opening, closing, high, and low prices of the S&P 500 stock index. I saved this data to a .csv file. 

## **SP500_monthly_data.csv** <br>
I utilized the Yahoo Finance API to find the closing prices of the S&P 500 stock index. The dates present for the S&P 500 data were from January 1929 to March 2025. I found the opening, closing, high, and low prices of this stock. After obtaining this information, I narrowed the data to the closing price at the end of the month, and I rounded it to two decimal places. I shifted all the monthly data from the first to the last of the month and converted the column to a datetime data type. After this step, the columns present for each stock were “Date” and “Ticker,” with the ticker being the symbol for each stock. The “Ticker” column was already a float data type. I saved this data to a .csv file. 

## **NASDAQ_data.csv**
I utilized the Yahoo Finance API to find the opening, closing, high, and low prices of the Nasdaq stock index. I saved this data to a .csv file. 

## **NASDAQ_monthly_data.csv**<br>
I utilized the Yahoo Finance API to find the closing prices of the Nasdaq stock index. The Nasdaq Composite stock contained dates from February 1971 to December 2023. I found the opening, closing, high, and low prices of this stock. After obtaining this information, I narrowed the data to the closing price at the end of the month, and I rounded it to two decimal places. I shifted all the monthly data from the first to the last of the month and converted the column to a datetime data type. After this step, the columns present for each stock were “Date” and “Ticker,” with the ticker being the symbol for each stock. The “Ticker” column was already a float data type. I saved this data to a .csv file. 

## **DowJones_data.csv**
I utilized the Yahoo Finance API to find the opening, closing, high, and low prices of the Dow Jones stock index. I saved this data to a .csv file. 

## **DowJones_monthly_data.csv**<br> 
I utilized the Yahoo Finance API to find the closing prices of the Dow Jones stock index. The dates present for the Dow Jones stock were from January 1992 to December 2023. I found the opening, closing, high, and low prices of this stock. After obtaining this information, I narrowed the data to the closing price at the end of the month, and I rounded it to two decimal places. I shifted all the monthly data from the first to the last of the month and converted the column to a datetime data type. After this step, the columns present for each stock were “Date” and “Ticker,” with the ticker being the symbol for each stock. The “Ticker” column was already a float data type. I saved this data to a .csv file. 

## **sp_nasdaq_dowjones_combined.csv**<br> 
After utilizing the Yahoo Finance API for each stock I chose to analyze, I saved them to separate .csv files. I then horizontally merged the S&P 500 stock index data with the Nasdaq stock index data. I used an outer join and merged on the "Date" column. I saved this merged pandas DataFrame. After this step, I horizontally merged the S&P 500 and Nasdaq stock index data with the Dow Jones data. After this step, I had the final .csv file containing all of the stock indeces. 

## **Interest_Rates_Monthly.csv**<br> 
When searching for the interest rate data, I used a .csv file from the Federal Reserve Bank of St. Louis ([Federal Reserve Bank of St. Louis, Federal Funds Effective Rate, 2025](https://fred.stlouisfed.org/series/FEDFUNDS)). This website provided a graph and a file regarding the interest rates from the Board of Governors of the Federal Reserve. I gathered this data by downloading the .csv file attached to the website. The file contained the monthly interest rate from July 1954 to February 2025; there was an “observation_date” column and a “FEDFUNDS” column. I renamed the columns to “Date” and “Interest_Rate.” I shifted all the dates from the first to the last day of the month and converted them to a datetime data type to integrate later. The “Interest_Rate” column was already a float data type.

## **Inflation_Long_Rates.csv**<br>
When searching for the inflation rates, I scraped the U.S. Inflation Calculator website ([Coinnews Media Group LLC, 2025](https://www.usinflationcalculator.com/inflation/historical-inflation-rates/ )). There is a table with years to the left and months and averages as the columns; the data includes monthly inflation rates. The table contained data from January 1914 to February 2025. When writing the code, I found the table on the website using XPATH and then narrowed my search by looking for table rows using TAG_NAME. The year and month data were table headers, so I had to utilize the search for table headers using XPATH. The actual data, inflation rates per month, was table data, so I utilized XPATH to find this table data. I also initialized lists for each column, which were months and averages, to capture the scraped data. Following the initial data scraping, I created a pandas DataFrame to visualize all the data in the lists. After properly scraping all the data, I had to convert it from a wide format to a long format to match the layout of my other datasets. I removed the average column to include the accurate monthly data. I also removed a few rows at the end of the DataFrame because no dates were present. To obtain the proper dates, I mapped out month names to numbers, applied the mapping to the months, extracted the “Month” and “Year” columns, converted these columns to one column called “Date,” converted this “Date” column to a datetime datatype, and found the last day of each month to integrate all data later. In the end, the columns present were “Date” and “Inflation_Rate” because I renamed them. The “Inflation_Rate” column was already a float data type. I saved this data to a .csv file. 

## **historical_inflation_rates.csv**
After initially scraping the inflation calculator website, I created a .csv file for the original inflation rate data. The inflation rates are from January 1914 to March 2025. 

## **Unemployment_With_Stocks.csv**<br>
After merging the stock indeces into one pandas DataFrame, I horizontally merged this .csv file with the unemployment data. I used an outer join and merged on the "Date" column. I saved this merged pandas Dataframe to another .csv file. 

## **Unemployment_With_Stocks_Interest.csv**<br> 
After merging the unemployment and stock data, I then horizontally merged this new pandas DataFrame with the interest data. I used an outer join and merged on the "Date" column. I saved this merged pandas DataFrame to another .csv file. 

## **mscheitler_Unemployment_With_Stocks_Interest_Inflation.csv**<br> 
After merging the unemployment, stock, and interest data, I horizontally merged this new pandas DataFrame with the inflation data. I used an outer join and merged on the "Date" column. I saved this merged pandas DataFrame to another .csv file. 

## **mscheitler_Final_Cleaned_Dataset.csv**<br>
After merging all of my data into one final merged pandas DataFrame, I proceeded to remove NaN values for my final cleaned dataset. I saved this pandas DataFrame to the final .csv file I used in my analysis. 

# **Data Dictionary For All Columns in Final Dataset**

| Field | Type | Description |
| ------ | ------ | ------ |
| Date | Datetime | Date (year, month, day) - 1992 to 2025 |
| Unemployment_Rate | Float | Rate of Unemployment (percentage of people without jobs that could have jobs) |
| ^GSPC | Float | S&P 500 Stock Closing Price |
| ^IXIC | Float | Nasdaq Composite Stock Closing Price |
| ^DJI | Float | Dow Jones Stock Closing Price |
| Interest_Rate | Float | Interest Rate (percentage of a loan that is charged as interest to borrower) |
| Inflation_Rate | Float | Inflation Rate (percent change in the price of a basket of goods/services over a period of time) |
