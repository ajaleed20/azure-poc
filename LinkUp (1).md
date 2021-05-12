# Onboarding Notes On LinkUp

## DataSet Names
Following are data sets available for vendor Linkup
* JDE
  * CloudQuant
    * Feeds
  * Standard
    * Feeds
       * FS Daily Company Reference
       * Raw Daily Company Scrape Log
       * Raw Daily Job Records And Descriptions
       * Raw Daily PIT Company Reference
       * Raw Full Company Scrape Log
       * Raw Full Job Descriptions
       * Raw Full Job Records
       * Raw Full PIT Company Reference
       * Raw Full PIT Ticker Reference

    * MarketReports
      * Reports
        * Core_Company_Analytics
        * Core_Ticker_Analytics
    * Release Notes
      * 2-1
      * 2-1-1
## Date Range For DataSets
* Standard
  * Feeds
    * FS Daily Company Reference		(2019/11/07 till 2021/02/21) 
	* Raw Daily Company Scrape Log		(2019/04/24 till 2021/02/21)
	* Raw Daily Job Records And Descriptions	(2018/06/11 till 2021/02/21)
	* Raw Daily PIT Company Reference	(2019/04/22 till 2021/02/21)
	* Raw Full Company Scrape Log		(2018/05/31 till 2021/01/31)
	* Raw Full Job Descriptions		(2018/07/01 till 2021/01/31)
	* Raw Full Job Records			(2018/05/31 till 2021/01/21)
	* Raw Full PIT Company Reference	(2019/05/31 till 2021/01/31)
	* Raw Full PIT Ticker Reference		(2019/05/17 till 2020/01/01)
   * MarketReports
     * Reports
•	Core_Company_Analytics	(2019/11/13 till 2021/02/21)
•	Core_Ticker_Analytics		(2019/11/17 till 2021/02/21)
## Data Observation 
### Columns in DataSets:
* JDE
  * Standard
    * Feeds

**FS Daily Company Reference**
Columns List:
&nbsp;&nbsp;company_id
&nbsp;&nbsp;factset_entity_id
&nbsp;&nbsp;start_date
&nbsp;&nbsp;end_date
&nbsp;&nbsp;stock_ticker	
&nbsp;&nbsp;stock_exchange_country
&nbsp;&nbsp;stock_exchange_name
&nbsp;&nbsp;isin
&nbsp;&nbsp;cusip
&nbsp;&nbsp;sedol
&nbsp;&nbsp;primary_flag

**Raw Daily Company Scrape Log**
Columns List:
&nbsp;&nbsp;company_id
&nbsp;&nbsp;date
&nbsp;&nbsp;scrape_run_complete
&nbsp;&nbsp;scrape_changed

**Raw Daily Job Records And Descriptions**
Columns List:
&nbsp;&nbsp;hash
&nbsp;&nbsp;title
&nbsp;&nbsp;company_id
&nbsp;&nbsp;city
&nbsp;&nbsp;state
&nbsp;&nbsp;zip
&nbsp;&nbsp;country
&nbsp;&nbsp;created (timestamp)
&nbsp;&nbsp;last_checked (timestamp)
&nbsp;&nbsp;last_updated (timestamp)
&nbsp;&nbsp;delete_date
&nbsp;&nbsp;unmapped_location
&nbsp;&nbsp;onet_occupation_code

**Raw Daily PIT Company Reference**
Columns List:
&nbsp;&nbsp;company_id
&nbsp;&nbsp;start_date
&nbsp;&nbsp;end_date
&nbsp;&nbsp;company_name
&nbsp;&nbsp;company_url
&nbsp;&nbsp;lei
&nbsp;&nbsp;open_perm_id
&nbsp;&nbsp;naics_code

**Raw Full Company Scrape Log**
Columns List
&nbsp;&nbsp;company_id
&nbsp;&nbsp;date
&nbsp;&nbsp;scrape_run_complete
&nbsp;&nbsp;scrape_changed

**Raw Full Job Descriptions**
Very big xml files, in GBz. Downloaded a 40GB tar file in which found some xml files of more than 10GB each.
e.g. ‘linkup_job_descriptions_2018-07-01_1’ , ‘linkup_job_descriptions_2018-07-01_0.xml’
inside tar file ‘linkup_job_descriptions_2018-07-01.tar.gz’

**Raw Full Job Records**
Columns List
&nbsp;&nbsp;hash
&nbsp;&nbsp;title
&nbsp;&nbsp;company_id
&nbsp;&nbsp;company_name
&nbsp;&nbsp;city
&nbsp;&nbsp;state
&nbsp;&nbsp;zip
&nbsp;&nbsp;country
&nbsp;&nbsp;category_id
&nbsp;&nbsp;category_name
&nbsp;&nbsp;created
&nbsp;&nbsp;last_checked
&nbsp;&nbsp;last_updated
&nbsp;&nbsp;unmapped_location

**Raw Full PIT Company Reference**
Columns List
&nbsp;&nbsp;company_id
&nbsp;&nbsp;start_date
&nbsp;&nbsp;end_date
&nbsp;&nbsp;company_name
&nbsp;&nbsp;company_url
&nbsp;&nbsp;lei
&nbsp;&nbsp;open_perm_id
&nbsp;&nbsp;naics_code

**Raw Full PIT Ticker Reference**
Columns List
&nbsp;&nbsp;company_id
&nbsp;&nbsp;start_date
&nbsp;&nbsp;end_date
&nbsp;&nbsp;stock_ticker
&nbsp;&nbsp;stock_exchange
&nbsp;&nbsp;country
&nbsp;&nbsp;stock
&nbsp;&nbsp;exchange_name
&nbsp;&nbsp;primary_flag


JDE
* Standard
  *	MarketReports
    * Reports

**Core_Company_Analytics**
Columns List
&nbsp;&nbsp;company_id
&nbsp;&nbsp;start_date
&nbsp;&nbsp;end_date
&nbsp;&nbsp;stock_ticker
&nbsp;&nbsp;stock_exchange
&nbsp;&nbsp;country
&nbsp;&nbsp;stock
&nbsp;&nbsp;exchange_name
&nbsp;&nbsp;primary_flag

**Core_Ticker_Analytics**
Columns List
&nbsp;&nbsp;day
&nbsp;&nbsp;stock_ticker
&nbsp;&nbsp;created_job_count
&nbsp;&nbsp;deleted_job_count
&nbsp;&nbsp;unique_active_job_count
&nbsp;&nbsp;active_duration

## Data Details In Release Notes
### ReleaseNotes 2-1:
This 2.1 release is focused on convenience of data ingestion and mapping.
#### Reference Material and Files
General
All reference files will be filtered so that only companies with at least 1 job record will be included in a file.
Fixed a bug where some companies that had job records were not being included in the reference files.

NEW FILE:  **fs_company_reference_daily**
Description:  We have concorded our companies to FactSet Entity ID.  We then climb the hierarchy to get relevant identifiers and supplemental reference material to be used for mapping purposes.
 Columns
&nbsp;&nbsp;company_id
&nbsp;&nbsp;factset_entity_id
&nbsp;&nbsp;start_date
&nbsp;&nbsp;end_date
&nbsp;&nbsp;stock_ticker
&nbsp;&nbsp;stock_exchange_country
&nbsp;&nbsp;stock_exchange_name
&nbsp;&nbsp;isin
&nbsp;&nbsp;cusip
&nbsp;&nbsp;sedol
&nbsp;&nbsp;primary_flag
Stocks include Shares and ADR's
OTC stocks are included with a stock exchange of OTC

**PIT Company Reference File**
Previously all company reference dates started in February of 2016.  Rows will be added so no manipulation to the dates needs to be done to do a standard DATE BETWEEN join by backfilling values. The earliest start date for a company will correspond to when that company was created in our system, which will always be before the scrape was created and started.
Quant/Analytics/Aggregated Data Files
Quant Files are being deprecated.  This is being replaced by the new core_company_analytics file described below.  All information and data in these 4 files will be included in the new core_company_analytics file 

NEW FILE: **core_company_analytics**
Description:  This file replaces the 4 "Quant" files previously.  It contains all the data of those 4 file, but it has been combined into 1 for convenience.
Columns
&nbsp;&nbsp;day
&nbsp;&nbsp;company_id
&nbsp;&nbsp;company_name
&nbsp;&nbsp;created_job_count
&nbsp;&nbsp;deleted_job_count
&nbsp;&nbsp;active_job_count	
&nbsp;&nbsp;active_duration
Any row with no data will not be written.  For example, if a company has no active, created, or deleted jobs the row will not be written.  Previously all dates in the range were written for each company ID and filled in with 0’s.
Each file will include data from 2007 - Present.  Previous "Quant" file data started in 2012.

NEW FILE: **core_ticker_analytics**
Description:  This is a new file that will be similar to core_company_analytics, but grouped by Ticker instead of comapany_id.
Columns
&nbsp;&nbsp;day
&nbsp;&nbsp;stock_ticker
&nbsp;&nbsp;created_job_count
&nbsp;&nbsp;deleted_job_count
&nbsp;&nbsp;active_job_count	
&nbsp;&nbsp;active_duration
Any row with no data will not be written.  For example, if a company has no active, created, or deleted jobs on a specific day the row will not be written.Previously all dates in the range were written for each company ID and filled in with 0’s.
Each file will include data from 2007 - Present.

### ReleaseNotes 2-1-1:
The release notes are focused on improving consistency of the file naming convention
Naming Convention for LinkUp Raw Files   

**Raw Full PIT Company Reference File**

Current State:  Filename is dated one day after the data in the file.	 
         Example raw_pit_company_reference_full_2020_01_01.csv.gz 
         latest time stamp is 2019-12-31 (data through the 31  not the 1 ). 

Future State:    Filename is dated day of the data in the file
        Example raw_pit_company_reference_full_2019_12_31.csv.gz 
        latest time stamp is 2019 -12-31 (data through the 31 ). 

**Raw Daily PIT Company Reference File**

Current State: Filename is dated one day after the data in the file
.	         Example raw_pit_company_reference_daily_2020_01_05.csv.gz 
         latest time stamp is 2020-01-04 (data through the 4th not the 5 ). 

Future State:  Filename is dated day of the data in the file
	        Example raw_pit_company_reference_daily_2020_01_04.csv.gz 
       latest time stamp is 2020-01-04 (data through the 4 ). 
 
**Raw Full Job Records** 

Current State: Filename is dated day of the data in the file. Data is placed in 
        JDE/Standard/Feeds/Raw Full Job Records/2020/01/ 
        with file date of raw_job_archive_2019_12_31.tar.gz 

Future State:  Data will be placed in JDE/Standard/Feeds/Raw Full Job Records/2019/31/	 
	        with a file date of raw_job_archive_2019_12_31.tar.gz 

**Raw Full Job Descriptions** 

Current State: Filename is dated one day after the data in the file. Data is placed in 
	        JDE/Standard/Feeds/Raw Full Job Descriptions/2020/01/	 
		        with file date of linkup_job_descriptions_2020-01-01.tar.gz 

Future State: Data will be placed in JDE/Standard/Feeds/Raw Full Job Descriptions/2019/31/ 
	                     with a file date of linkup_job_descriptions_2019-12-31.tar.gz 

**Raw Full Company Scrape Log**  

Current State: Filename is dated two days after the data in the file.	 
                      Example the file generated on November 1, 2019 that includes data through	 
       October 31, 2019 is uploaded to the location JDE/Standard/Feeds/Raw Full 
                     Company Scrape Log/2019/11/raw_company_scrape_log_full_2019-11-01.csv.gz 

Future State: Example above file will be JDE/Standard/Feeds/Raw Full Company Scrape	 
Log/2019/10/raw_company_scrape_log_full_2019-10-31.csv.gz 
 
**Raw Daily Company Scrape Log**

Current State: Filename is dated two days after the data in the file.
	         Example raw_company_scrape_log_daily_2019-11-06.csv.gz 
         contains scrape log records for the day 2019-11-04. 

Future State:  Filename is dated day of the data in the file.
	        Example raw_company_scrape_log_daily_2019-11-04.csv.gz 
        contains scrape log dates for the day 2019-11-04. 
 
**Company and Ticker Analytic Files** 

Current State: Filename is dated day of the data in the file.
                       Example core_company_analytics_2020-01-16.csv.gz 
	                      contains company analytics  for the day 2019-01-16. 
        Example core_ticker_analytics_2020-01-16.csv.gz 
        contains ticker analytics for the day 2019-01-16. 

Future State: No change	 
 
**Raw Daily Job Records**

Current State: Filename is dated day of the data in the file.
	                       Example raw_daily_2019-12-14 
                       contains daily data for the day	 2019-12-14 

Future State:  No change	

