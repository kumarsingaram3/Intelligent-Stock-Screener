# Clustering-Stock-Screener

Building a stock screening tool using KMeans clustering to help investors speed up their investment process and identify overlooked opportunities in the market

## Project Description

There are many tools investors use to both discover and analyze different potential investments. One popular tool for discovery & analysis is the stock screener. This tool helps investors narrow down potential investments based on their own criteria. The criteria filter could be placed on anything from how fast the company grows sales to one specific industry the investor wants to analyze.

The problem with the stock screener is that companies are grouped in a rule based way. What if we could instead, group potential investments algorithmically, allowing companies to cluster naturally with one another based on their individual characteristics? To solve this problem, we will be using a popular unsupervised learning algorithm known as a K-Means to build an investment tool integrated with Power BI to help investors speed up their investment process and identify overlooked opportunities in the market relative to their true peer group.

## Technologies

* Python
* Pandas
* Numpy
* Seaborn
* Jupyter
* Sklearn
* BeautifulSoup

## Methods

* Web Scraping
* Feature Engineering
* Data Visualization
* Unsupervised Learning Techniques
* Investment Research

## How to Use K-Means Clustering Stock Screener

Below are the instructions for how to use the K-Means Clustering Stock Screener. 

### Installation & Instructions

**To run the script that refreshes with the latest financial information from Yahoo Finance:**

* Clone this repo to your computer
* Install necessary packages noted under Technologies
* Save [ticker_list.csv](https://github.com/kumarsingaram3/Clustering-Stock-Screener/blob/main/ticker_list.csv) to your computer (update ticker data as desired)

**To learn how to use the stock screening tool, follow the instructions below:**

The first two sections cover both tabs within the stock screener. The final section reviews all the financial terminology used in the tool.

**Tab 1 – Screener**

**Choose Group:**
There are 11 total groups to choose from. Each group has a set of characteristics associated with it, based on a company’s Gross Margin, Operating Margin, Research & Development, General Administrative Expenses, Free Cash Flow, Capital Expenditures, 3 Year Average Sales Growth, and 3 Year Average Net Income Growth.

Each group of companies is defined below:

•	Cluster 0 - Low Margin Grind: These companies are in competitive industries without much room for error.\
•	Cluster 1 - Steady Compounders: These are steady businesses mostly in the mature phase of their company's life cycle.\
•	Cluster 2 - R&D Heavy Compounders: These companies have skill and/or proprietary based advantages over their competitors.\
•	Cluster 3 - Capital Intensive Compounders: These businesses spend a lot on CapEx, making them expensive to compete with.\
•	Cluster 4 - Raising Prices: No group has grown earnings faster. These companies are in the process of monetizing their customers.\
•	Cluster 5 - Venture Style Growth: Fast growth and high margins allow these businesses to reinvest all their earnings.\
•	Cluster 6 - R&D Charged Growth: These companies have skill/proprietary advantages allowing them to take share and/or raise prices.\
•	Cluster 7 - Efficient Compounders: These companies have no issues making money. They spend little on CapEx, R&D, and G&A.\
•	Cluster 8 - Taking Share: These companies provide expensive/subsidized services to their customers, allowing them to grow faster.\
•	Cluster 9 - No Man's Land: The oddball companies. There's no one else like 'em.\
•	Cluster 10 - Taking Profits: Many of these companies have either begun to show saturation or have saturated their respective markets.

Users can pick one or more groups as a starting point for their research. Note that these definitions do not necessarily encompass every company within a cluster group. They merely represent the median company profile of each group.

**Stock Ticker:**

Users can scroll to choose a specific stock ticker using this filter. This will populate the data on both tabs for only the chosen stock ticker. This can be used to view a company’s numbers on its own or check the group that a particular company falls into.

**Market Cap:** The slider can be used to analyze companies within a specific range of market caps. 

**Sales Growth:** Filter companies based on their 3-year average sales growth

**Net Income Growth:** Filter companies based on their 3-year average net income growth

**Price to Earnings:** Filter companies based on their price to earnings ratio

**Price to Sales:** Filter companies based on their price to sales ratio

The company overview table provides high level details of each company including its Cluster Group, Market Capitalization, Price to Sales (PS), Price to Earnings (PE), 3-Year Average Sales Growth, 3-Year Average Net Income Growth, PSG Ratio, and PEG Ratio. To sort the table by a specific column, users can click the column headers.

**Tab 2 – Detail**

The detail tab reflects filters set in Cluster Group, Stock Ticker, and Market Cap chosen on the first tab. If the user selects a specific ticker on tab 1, the ticker should be reflected on the detail tab as well. This tab allows users to dig deeper into the efficiency and value of a company based on different metrics. 

**Valuation Metrics:**

Price to Gross Profit (PGP), Price to Free Cash Flow (PFCF), PGPG, and PFCFG are ratios to evaluate companies of different types. PGPG and PFCFG specifically, are ratios that adjust PGP and PFCF for growth. Meaning, companies that have grown very faster in either area, would have a lower PGPG and PFCFG.

**Growth Metrics:**

Metrics such as RORD (Return on Research & Development) and GAEFF (General & Administrative Efficiency) can be applied to growing companies or companies that are oriented towards research or consulting. The cluster group chosen can be a guide for which metric is the most applicable to a set of companies.
For example, RORD is the most applicable on cluster groups like R&D Charged Growth and R&D Heavy Compounders. This is because the companies within these groups rely on R&D to drive sales/profitability.

Some companies are more sales oriented, which is where GAEFF can be an effective metric to use. For example, Software as a Service companies typically employ many salespeople that are used to sell the company’s software products. A company with a higher GAEFF may indicate that a company is able to sell its products more efficiently.

**Profitability Metrics:**

Metrics such as ROE, ROA, ROIC, ROIIC, Reinvestment Rate, and Compounding Rate are often used by value investors to get a sense of how efficiently a company can generate profits. These metrics are better suited for mature companies that consistently show profits. However, because many companies in the markets today have more intangible than tangible assets, these metrics may not always apply. Once again, the clusters can be used as a guide for when these may be relevant to the company being assessed. 

**Financial Metrics Defined**

Below is all financial terminology used in the Stock Screener defined:

**Mkt Cap:** Size of a company, as defined by - *Shares Outstanding x Price Per Share*\
**PS:** *Mkt Cap/Trailing 12 Month Revenue*\
**PE:** *Mkt Cap/Trailing 12 Month Net Income*\
**PGP:** *Mkt Cap/Trailing 12 Month Gross Profit*\
**PFCF:** *Mkt Cap/Trailing 12 Month Free Cash Flow*\
**Sales Growth:** 3-year average sales growth\
**Net Income Growth:** 3-year average net income growth\
**GP Growth:** 3-year average gross profit growth\
**FCF Growth:** 3-year average free cash flow growth\
**GM%:** Gross Margin %\
*Gross Profit/Total Revenue*\
**OP%:** Operating Margin %\
*Operating Income/Total Revenue*\
**PEG:** *PE/Net Income Growth*\
**PSG:** *PS/Sales Growth*\
**PGPG:** *PGP/GP Growth*\
**PFCFG:** *PFCF/FCF Growth*\
**RORD:** Return on Research & Development\
*[(Gross Profit – Gross Profit (3 Years Prior)) – (G&A – G&A (3 Years Prior))]/Cumulative 3 Year R&D*\
**GAEFF:** General & Administrative Efficiency\
*[Gross Profit – Gross Profit (3 Years Prior)]/[G&A – G&A (3 Years Prior)]*\
**FCF/NI:** *Cumulative 3 Year Free Cash Flow/Cumulative 3 Year Earnings Before Interest & Tax*\
**ROE:** Return on Equity\
*Net Income/Shareholder’s Equity*\
**ROA:** Return on Assets\
*Net Income/Current Assets*\
**ROIC:** Return on Invested Capital\
*EBIT/(Long Term Debt + Shareholder’s Equity – Cash)*\
**ROIIC:** Return on Incremental Invested Capital\
*[EBIT – EBIT (3 Years Prior)]/[(Long Term Debt + Shareholder’s Equity – Cash) – (Long Term Debt (3 Years Prior) + Shareholder’s Equity (3 Years Prior) – Cash (3 Years Prior)]*\
**Rvst. Rate:** Reinvestment Rate\
*[Retained Earnings – Retained Earnings (3 Years Prior)]/Cumulative 3 Year Earnings Before Interest*\
**Comp. Rate:** Compounding Rate\
*ROIIC x Rvst. Rate*\
**Turnover:** *Total Revenue/(Long Term Debt + Shareholder’s Equity – Cash)*\
**D/E:** Debt to Equity\
*(Long Term Debt + Short Term Debt)/(Shareholder’s Equity)* 


