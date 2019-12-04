# Financial Rating System for Turkish Firms Project
Financial rating (from AAA to C) prediction system using selected financial ratios for Turkish private and public companies.

## Project Purpose
The purpose of the project is predicting financial ratings of Turkish companies by using liquidity & debt & profitability ratios calculated from last 12 months (LTM) balance sheet and income statements.

There are 6 classes of financial ratings in this project: AAA-AA, A-BBB, BB, B, CCC, CC-C.

One of the purposes of giving financial rating to a firm is to better compare financial performance of the firm with that of global firms and it local competitors from same industry.

Another benefit of giving financial rating to a firm is that it helps better understand financial performance of the firm from people who are not financial literate or who have limited understanding of balance sheet and income statement.

## Featured Notebooks
* [Exploratory Data Analysis](https://github.com/dorukcanga/Financial-Rating-System-for-Turkish-Firms/blob/master/Data_Cleansing_and_Exploratory_Analysis.ipynb)
* [Training of Unsupervised Learning Models](https://github.com/dorukcanga/Financial-Rating-System-for-Turkish-Firms/blob/master/Clustering_Model_Training.ipynb)

## Dataset
Dataset consists of June 2018-June 2019 LTM balance sheet and income statement informations of more than 40000 public companies from all over the world. Data is obtained from Thomson Reuters.

### Features of the raw dataset:
* Company Code
* Company Name
* Country of Headquarters
* Industry Name
* Income Statement Features: Revenue, Gross Profit, EBITDA, EBIT, Net Income
* Balance Sheet Features: Total Assets, Current Assets, Cash & Short Term Investments, Accounts Receivable, Inventory, Total Liabilities, Current Liabilities, Accounts Payable, Total Debt, Total Equity, Interest Income & Expense
* Country Tax Rates

## Financial Ratios and Explanations
Following financial ratios are calculated and analyzed:
* [Current Ratio](https://www.investopedia.com/terms/c/currentratio.asp)
* [1 to Working Capital Turnover](https://www.investopedia.com/terms/w/workingcapitalturnover.asp)
* [Cash Conversion Cycle](https://www.investopedia.com/terms/c/cashconversioncycle.asp)
* [Total Debt to Total Assets](https://www.investopedia.com/terms/t/totaldebttototalassets.asp)
* [Total Debt to Total Equity](https://www.investopedia.com/terms/d/debtequityratio.asp)
* [1 to Interest Coverage Ratio](https://www.investopedia.com/terms/i/interestcoverageratio.asp)
* [Net Debt to EBIT](https://www.investopedia.com/terms/n/net-debt-to-ebitda-ratio.asp)
* [Gross Profit Margin](https://www.investopedia.com/terms/g/gross_profit_margin.asp)
* [EBITDA Margin](https://www.investopedia.com/terms/e/ebitda-margin.asp)
* [EBIT Margin](https://www.investopedia.com/terms/o/operatingmargin.asp)
* [Net Profit Margin](https://www.investopedia.com/terms/n/net_margin.asp)
* [Return on Invested Capital](https://www.investopedia.com/terms/r/returnoninvestmentcapital.asp)
* [Return on Equity](https://www.investopedia.com/terms/r/returnonequity.asp)
* [Return on Asset](https://www.investopedia.com/terms/r/returnonassets.asp)
* [Asset Turnover Rate](https://www.investopedia.com/terms/a/assetturnover.asp)

**Selected Ratios for Model Training:** Current Ratio, 1 to Working Capital Turnover, Total Debt to Total Assets, Net Debt to EBIT, EBIT Margin, Return on Invested Capital

## Project Outline
### Data Preprocessing:
* Extracting unused industries:

Financial Institutions, Investment Companies & Trusts, Holding Companies are excluded from this analysis.

* Extracting selected countries:

Countries that most of their companies finance their operations without interest are excluded from dataset.

* Extracting companies with IPO in one year:

Companies went public after June 2018 are exluded from this analysis.

* Deleting companies with missing values.

Companies that have missing values in important financial data even if they are public extracted from dataset.

### Financial Ratios:

Financial ratios listed above are calculated.

### Outlier Analysis:

Strong outliers are exctracted from dataset because most of them are extreme cases or wrong records.

### Exploratory Data Analysis:

* Correlogram, histograms, boxplots and joint plots of ratios
* Boxplots of ratios by industries and countries

### Unsupervised Learning Model Evaluations

KMeans, Agglomerative Clustering, Gaussian Mixture and KPrototype models are implemented.

Results are analyzed with Silhouette Score Curves, Cluster Center Plots and Silhouette Graph of Clusters. Also ratings of selected Turkish public companies from different industries are analyzed to compare performances of the models.

KPrototype model is selected as final model and ratings of more than 20 private companies given by KPrototype model are analyzed as a final test. (Private company analysis is excluded from the code due to confidentiality issues)









