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
1) **Optional (if needed):** Navigate to the folder and run the *setup.bat* file inside the *BrokerCheck_Scraper* folder, only if the requirements are not met (see below). **Note,** the setup only needs to be run once per computer!

2) Make sure you have all of the requirements met, then double-click on *BCScrapeRunner.bat* to start the program. A terminal window should open upon success, and soon after should follow an import file window. 

3) Import the CSV file (**not xlsx**, make sure to convert before), then enter the column name containing the CRDs. If it does not have a name, provide it with one. Make sure there is only CRDs in the selected column, without any blank cells in it, otherwise the program may run into an error. 

5) Wait and let the program run, do not close out of the chrome windows while in progress. Time may be slighly off and should only be used as an estimate.

6) When the program is complete, it will ask you to save the file. Input a name, choose a location, and select save. Then you are done! :thumbsup:
   
### Requirements
Not included with setup.bat install:
 - [python 3.8+](https://www.python.org/downloads/release/python-3111/#:~:text=Windows%20installer%20(64%2Dbit))
 - [pip (python package installer)](https://www.geeksforgeeks.org/how-to-install-pip-on-windows/#:~:text=Step%201%3A%20Download%20the%20get,where%20the%20above%20file%20exists.&text=Step%204%3A%20Now%20wait%20through,Voila!)
 - [Google Chrome](https://support.google.com/chrome/answer/95346?hl=en&co=GENIE.Platform%3DDesktop#zippy=%2Cwindows:~:text=Download%20the%20installation%20file)

Included with setup.bat install:
 - pandas
 - numpy
 - selenium
 - tkinter (tk)
 - Beautiful Soup 4 (bs4)
 - openpyxl
 - requests
 
### Important
When downloading python, make sure to select **Add python to PATH**. If you forget to do so, you can reinstall, or [follow this tutorial](https://www.youtube.com/watch?v=4bUOrMj88Pc).

To ensure that your python install was successful, type *python* or *python3* into the command prompt. 
   - If there is output ending in **>>>**, then it was successful, you can exit by typing *exit()* and hitting enter, or by closing the window. 
   - If you recieve a message stating, "'python' is not recognized as an internal command...", then it was unsuccessful. You can fix this issue by following the tutorial link directly above. 
