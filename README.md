# FINRA's BrokerCheck® Web Scraper
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/release/python-380/) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Web scraping application to automate data collection with FINRA's BrokerCheck®. Import a CSV file containing broker CRDs and this will scrape the website for individual data and will return an excel file containing the scraped and interpreted data.

## Data collected
 - Broker Name
 - Broker Firm 
   - Firm Address
   - Firm CRD
 - Broker Status 
   - Registered or not as broker or an investment adviser
 - Broker Information 
   - Years of Experience
   - Number of Firms
   - Number of Disclosures

The excel file will return columns with all of this information including highlighting on specific rows: 
```
Red = Not a Broker or Investment Advisor
Yellow = An Investment Advisor but not a Broker
Purple = Either only an Investment Advisor, or an incorrect CRD
```
## Instructions
1) Optional: Navigate to the folder and run the setup.bat file inside BrokerCheck_Scraper folder (if requirements not met, see below). 

2) Make sure you have all of the requirements met, then click on "BCScrapeRunner.bat" to start the program. 

3) Import the CSV file (not xlsx, make sure to convert before), then enter the name of the column containing the CRDs. If it does not have a name, provide it with one. Make sure there is only CRDs in the given column, otherwise an error will be thrown. 

5) Wait and let the program run, do not close out of the chrome windows while in progress. Time may be slighly off and should only be used as an estimate.

6) When the program is complete, it will ask you to save the file. Input a name and select save. Then you are done!
   
### Requirements
Not included with setup.bat install
 - python 3.8+
 - pip 
 - Google Chrome

Included with setup.bat install
 - pandas
 - numpy
 - selenium
 - tkinter (tk)
 - Beautiful Soup 4 (bs4)
 - openpyxl
 - requests
