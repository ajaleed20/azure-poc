# Onboarding Notes On LinkUp
CloudQuant's vendor: "LinkUp" has built the world’s most extensive, accurate, and up-to-date set of jobs direct from employer websites. With the largest and highest quality job listings index of 5 million job openings sourced from 50,000 company websites globally, LinkUp has become a leading provider of job market data and analytics. From that robust and unique dataset of jobs, LinkUp has developed Market Reports which delivers brilliant insights into the job market.
Market Reports is a SaaS application that allow users to create reports that extract real-time and historical job market data, resulting in powerful insights tailored to specific requirements. The reports can range in scope, are easy to build, completely customizable, and can be delivered in a variety of formats.

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

* company_id (string/varchar)
The unique identifier for each company-scrape
* factset_entity_id (string/varchar)
concorded our companies to FactSet Entity ID
* start_date (date)
The start date for this row. This is used for joining point-in-time information. Please see the join tutorial for assistance with join.
* end_date (date)
The end date for this row. This is used for joining point-in-time information. Please see join tutorial for assistance with join.
* stock_ticker (string/varchar)
The Ticker Symbol
* stock_exchange_country (string/varchar)
The country of the stock exchange that the ticker symbol is traded on.
* stock_exchange_name (string/varchar)
The stock exchange symbol that the ticker is traded on.
* isin (string/varchar)
International Securities Identification Number, mapped using FactSet
* cusip (string/varchar)
Committee on Uniform Securities Identification procedures number, mapped via FactSet.
* sedol (string/varchar)
Committee on Uniform Securities Identification procedures number, mapped via FactSet.
* primary_flag (boolean)
If True, this is the primary SEDOL for the company_id.

**Raw Daily Company Scrape Log**
Columns List:
* company_id (string/varchar)
The unique identifier for job records. This is used to join to reference files or aggregates.
* date (date)
The date the change occurred for the scrape.
* scrape_run_complete (boolean)
If True, this indicates the company-id was scraped on this date
* scrape_changed (boolean)
If True, this indicates that the code was modified for the scrape on this date

**Raw Daily Job Records And Descriptions**
Columns List:
* hash (string/varchar)
The unique identifier for job records. This is used to join job descriptions to job records.
* title (string/varchar)
Job title scraped from the unique url for the job post
* company_id (string/varchar)
Unique identifier for a company-scrape. This is is used to join to reference files with job records.
* city (string/varchar)
City location for the job posting.
* state (string/varchar)
State or region for the job posting.
* zip   (string/varchar)
Postal code for the job posting.
* country   (string/varchar)
* created (timestamp)
The first time this job was observed and scraped.
* last_checked (timestamp)
The most recent time this site was scraped and this job posting was observed.
* last_updated (timestamp)
The most recent time that this site was scraped and observed a change in the job posting.
* delete_date   (timestamp)
The most recent time this site was scraped and this job posting was not found.
* unmapped_location (boolean)
If True, this indicates that the job posting location was not able to be accurately identified.
* onet_occupation_code  (string)
The ONET classification of the job. It is one way of normalizing job titles.
* url (string)
The unique URL for the job posting.

**Raw Daily PIT Company Reference**
Columns List:
* company_id (stringg/varchar)
The unique identifier for job records. This is used to join to reference files or aggregates.
* start_date (date)
The start date for this row. This is used for joining point-in-time information. Please see the join tutorial for assistance with join. 
* end_date (date)
The end date for this row. This is used for joining point-in-time information. Please see join tutorial for assistance with join.
* company_name  (string/varchar)
The name for the company_id.
* company_url   (string/varchar)
The URL for the company_id.
* lei   (sting/varchar)
Legal Entity Identifier
* open_perm_id  (string/varchar)
Open source company identifier used for joining to other data.
* naics_code    (string/varchar)
Industry classification. This can be used to join to the Bureau of Labor Statistics salary data. 

**Raw Full Company Scrape Log**
Columns List
* company_id (string/varchar)
The unique identifier for job records. This is used to join to reference files or aggregates.
* date (date)
The date the change occurred for the scrape.
* scrape_run_complete   (boolean)
If True, this indicates the company-id was scraped on this date
* scrape_changed (boolean)
If True, this indicates that the code was modified for the scrape on this date

**Raw Full Job Descriptions**
Very big xml files, in GBz. Downloaded a 40GB tar file in which found some xml files of more than 10GB each.
e.g. ‘linkup_job_descriptions_2018-07-01_1’ , ‘linkup_job_descriptions_2018-07-01_0.xml’
inside tar file ‘linkup_job_descriptions_2018-07-01.tar.gz’

**Raw Full Job Records**
Columns List
* hash (string/varchar)
The unique identifier for job records. This is used to join job descriptions to job records.
* title (string/varchar)
Job title scraped from the unique url for the job post
* company_id (string/varchar)
Unique identifier for a company-scrape. This is is used to join to reference files with job records.
* company_name (string/varchar)
This is the name of the company pertaining to the company_ID.
* city (string/varchar)
City location for the job posting.
* state (string/varchar)
State or region for the job posting.
* zip (string/varchar)
Postal code for the job posting.
* country (string/varchar)
* category_id
* category_name
* created (timestamp)
The first time this job was observed and scraped.
* last_checked (timestamp)
The most recent time this site was scraped and this job posting was observed.
* last_updated (timestamp)
The most recent time that this site was scraped and observed a change in the job posting.
* unmapped_location (boolean)
If True, this indicates that the job posting location was not able to be accurately identified.

**Raw Full PIT Company Reference**
Columns List
* company_id (string/varchar)
The unique identifier for job records. This is used to join to reference files or aggregates.
* start_date (string/varchar)
The start date for this row. This is used for joining point-in-time information. Please see the join tutorial for assistance with join. 
* end_date (string/varchar)
The end date for this row. This is used for joining point-in-time information. Please see join tutorial for assistance with join.
* company_name (string/varchar)
The name for the company_id.
* company_url (string/varchar)
The URL for the company_id.
* lei (string/varchar)
Legal Entity Identifier
* open_perm_id (string/varchar)
Open source company identifier used for joining to other data.
* naics_code (string/varchar)
Industry classification. This can be used to join to the Bureau of Labor Statistics salary data. 

**Raw Full PIT Ticker Reference**
Columns List
* company_id (string/varchar)
The unique identifier for job records. This is used to join to reference files or aggregates.
* start_date (date)
The start date for this row. This is used for joining point-in-time information. Please see the join tutorial for assistance with join. 
* end_date (date)
The end date for this row. This is used for joining point-in-time information. Please see join tutorial for assistance with join.
* stock_ticker (string/varchar)
The ticker symbol
*stock_exchange_country (string/varchar)
The country of the stock exchange that the ticker symbol is traded on.
* stock_exchange_name (string/varchar)
The stock exchange symbol that the ticker is traded on.
* primary_flag (boolean)
If True, this is the primary ticker for the company_id.


JDE
* Standard
  *	MarketReports
    * Reports

**Core_Company_Analytics**
Columns List
* company_id (string/varchar)
The unique identifier for each company-scrape
* company_name (string/varchar)
Readable name of the company
* day (date)
Date that the row applies to. 
* created_job_count (integer)
The number of jobs that were created on that day. This is measured by the number of unique job URLs on a career site that our scrape found.
* deleted_job_count (integer)
This is measured by the number of unique job URLs that are no longer on a career site that were on the career site on the previous scrape.
* unique_job_count (integer)
This is the number of active jobs on that day. This is measured by the number of unique active job URLs on career sites. 
* active_duration (decimal/float)
The mean of the duration (today – job creation date) in days for all jobs that are active on this day. For this calculation the max duration is 180 days.

**Core_Ticker_Analytics**
Columns List
* day (date)
Date that the row applies to. 
* stock_ticker (text/varchar)
This is the primary stock ticker for that row. Several company_ids may roll up to a single ticker. Format is stock_ticker | stock_exchange | stock_exchange_country. 
* created_job_count (integer)
The number of jobs that were created on that day. This is measured by the number of unique job URLs on a career site that our scrape found.
* deleted_job_count (integer)
This is measured by the number of unique job URLs that are no longer on a career site that were on the career site on the previous scrape.
* unique_active_job_count (integer)
This is the number of active jobs on that day. This is measured by the number of unique active job URLs on career sites. 
* active_duration (integr)
The mean of the duration (today – job creation date) in days for all jobs that are active on this day. For this calculation the max duration is 180 days.

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
* company_id
* factset_entity_id
* start_date
* end_date
* stock_ticker
* stock_exchange_country
* stock_exchange_name
* isin
* cusip
* sedol
* primary_flag
Stocks include Shares and ADR's
OTC stocks are included with a stock exchange of OTC

**PIT Company Reference File**
Previously all company reference dates started in February of 2016.  Rows will be added so no manipulation to the dates needs to be done to do a standard DATE BETWEEN join by backfilling values. The earliest start date for a company will correspond to when that company was created in our system, which will always be before the scrape was created and started.
Quant/Analytics/Aggregated Data Files
Quant Files are being deprecated.  This is being replaced by the new core_company_analytics file described below.  All information and data in these 4 files will be included in the new core_company_analytics file 

NEW FILE: **core_company_analytics**
Description:  This file replaces the 4 "Quant" files previously.  It contains all the data of those 4 file, but it has been combined into 1 for convenience.
Columns
* day
* company_id
* company_name
* created_job_count
* deleted_job_count
* active_job_count	
* active_duration

Any row with no data will not be written.  For example, if a company has no active, created, or deleted jobs the row will not be written.  Previously all dates in the range were written for each company ID and filled in with 0’s.
Each file will include data from 2007 - Present.  Previous "Quant" file data started in 2012.

NEW FILE: **core_ticker_analytics**
Description:  This is a new file that will be similar to core_company_analytics, but grouped by Ticker instead of comapany_id.
Columns
* day
* stock_ticker
* created_job_count
* deleted_job_count
* active_job_count	
* active_duration

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

## Details about LinkUp DataSets
# Job Record Definitions
A LinkUp Job Record is a record of a job posting from a company’s website or career portal. Each URL found counts as a unique job posting. LinkUp captures many data points when capturing job postings. Some of the more important data points are the dates when LinkUp found the job postings. LinkUp captures 4 important dates at this time:
* Created Date
This is the first date in which LinkUp found the URL. If this particular URL went up and down multiple times throughout a period of time, LinkUp uses the earliest known Created Date.
* Last Checked Date
This is the latest time the URL was verified to be active. Upon creation of a new posting, this date will match the Created Date. By default, LinkUp attempts to check all URLs once every 48 hours.
* Last Updated Date
This is the latest time the job posting has been modified. Upon creation of a new posting, this date will match the Created Date. Over time, as postings change their descriptions or titles, LinkUp updates this date to indicate changes have been made.
* Deleted Date
This is the date a posting has been removed from the website. If a job record has no Deleted Date, the posting is still active and on the website.

# Features and Filters of Market Reports
Market Reports is a feature of LinkUp’s Job Data Engine (JDE) product. This feature analyzes over 100 million job records and creates reports that are consumable in a spreadsheet format. Each report is a subset of the millions of data points calculated every day. These data points are created through aggregates.
* Aggregates
Aggregates are what defines how the job records are analyzed each day. A single new aggregate in the system could add hundreds of thousands of new data points to report from. An aggregate is comprised of 5 parts:
    * Filters
Filters are how the system determines which jobs should be analyzed. A good example of this would be the country filter. Perhaps you only want to analyze jobs that are in the U.S. because you’re looking for U.S. job market trends.
An aggregate can have many filters. In fact, LinkUp’s standard set of filters includes several that are aimed at getting rid of postings that are advertisements or possibly fabricated.
    * Dimensions
Dimensions are the properties of a job record that the aggregate is grouped by. The number of dimension types in the system is expandable, but the current list includes the following:
a) Company 
b) State (US only)
c) Digit NAICS
d) Digit NAICS
e) Category
f) Country
g) MSA
h) County (US only)
i) City

    * Primary Dimensions
      The primary dimension of an aggregate is the first grouping. This becomes a tab in an Excel formatted report, or the file name in a CSV style report. All counts or values shown on that tab are specific to that dimension value. As an example, if the “Primary Dimension” was “State,” a report could be constructed with a tab for each state within an Excel workbook. Where the CA tab only contains information about jobs in California, listed by a secondary dimension such as NAICS code or company. Note that you can choose “None” for the primary dimension, and this first grouping will simply not be done. 

    * Secondary Dimensions
    The secondary dimension is the second grouping. This becomes the row on each report. The same list of dimensions are available here. Continuing our example from above, if we chose “State” as our primary dimension and “Company” as our secondary dimension, we could construct a report for each state that has rows of values for each company. Note that for some dimensions a job record may not have a value. These jobs are then tallied under the “Other” row or tab.
    
* Aggregation Period
The Aggregation Period is really the third level of grouping. This determines the columns of a given report. Possible values for aggregate period are:
a) Daily
b) Weekly
c) Monthly
d) Quarterly
e) Yearly
This allows the system to aggregate job records over any period necessary. It can provide as granular as each day or as high level as each year. Continuing on our example if we choose Monthly for our Aggregate Period and keep the Dimensions as “State By Company,” the reports we construct from this Aggregate could have a tab for California (and all other states), a row for Target (and all other companies in our data set), and columns for each month.

* Metric Type
A Metric Type is what kind of analysis we’re doing. It determines what the value of a given cell means. To see explicitly how each of these are computed, see the Appendix. The current list of Metric Types are: 
a) Average Daily Active Job Count
b) Unique Active Job Count
c) Created Job Count
d) Deleted Job Count
e) Active Duration
f) Closed Duration
    * Average Daily Active Job Count
    This metric is an average of how many job postings were active for the given grouping. For example, if you were looking at a cell that represented the month of January 2012 for California and Target, this cell would indicate how many job postings were active, on average, per day in January of 2012 in California for Target.
    * Unique Active Job Count
This metric is a count of how many unique job postings were active for the given grouping. For example, if you were looking at a cell that represented the month of January 2012 for California and Target, this cell would indicate how many job postings were active in January of 2012 in California for Target
    * Created Job Count
    This metric is a count of how many new job postings were created for the given grouping. For example, if you were looking at a cell that represented the month of January 2012 for California and Target, this cell would indicate how many unique job postings were created in January of 2012 in California by Target.
    * Deleted Job Count
    This metric is a count of how many job postings were removed for the given grouping. For example, if you were looking at a cell that represented the month of January 2012 for California and Target, this cell would indicate how many job postings were removed in January of 2012 in California by Target.
    * Active Duration
    This metric is the average number of days each posting was active in a given grouping, only considering jobs that were active in the given period. For example, if you were looking at a cell that represented the month of January 2012 for California and Target, this cell would indicate the average number of days job postings were were active in January of 2012 in California by Target, for any and all postings that were active in January of 2012. Closed Duration This metric is the average number of days each posting was active in a given grouping, only considering postings that have closed in the given period. For example, if you were looking at a cell that represented the month of January 2012 for California and Target, this cell would indicate the average number days job postings were were active in January of 2012 in California by Target, for any and all postings that were taken down in January of 2012.

# Building a Market Report
Building a Market Report is easy, fast, and completely customizable. Reports are delivered as an Excel file with many tabs, or a zip archive of many CSV files. The data within them is always a subset of an Aggregate. A report is defined by 7 properties:
a) Aggregate
b) Schedule
c) Primary Dimension Values
d) Format
e) Secondary Dimension Values < Name
f) Date Range

* Primary Dimension Values
These are the values of the Primary Dimension this report will contain. This will be the explicit list of Excel tabs or CSV files contained in the final result. This allows for users to get only the subset of values they care to look at. It’s also important to be able to limit this, as certain Dimensions like County and MSA have hundreds or thousands of possible values. There is also a “select all” option, if the user simply wants every possible value.
* Secondary Dimension Values
These are the values of the Secondary Dimension this report will contain. This will be the explicit list of rows each tab or CSV file will contain. There is also a “select all” option, if the user simply wants every possible value.
* Date Range
The Date Range is the range of columns the report will contain. Based on the Aggregate selected, each column will be a Day, Week, Month, etc. This determines how wide each row will be. Currently the system allows any date range dating back to January 1, 2012. It can be specified either as an Absolute or a Relative range. Absolute allows a user to select a specific start and stop date for their report such as January 1, 2014 through January 1, 2016. Relative allows a user to select a rolling window of dates, such as 12 to 14 months ago. For reports running on a Schedule, the Relative Date Range is much more useful. Note: For absolute Date Ranges, the end date is exclusive. So if January 1, 2015 is selected as the end date, the report will contain all data up to January 1, 2015 at midnight UTC. That is, there will be no January 1, 2015 column on the report.
* Schedule
A Report may or may not have a Schedule. The schedule allows for a report to be run automatically after the nightly aggregation is complete. It’s possible to select a schedule that is Daily, Weekly, Monthly, Quarterly, or Yearly depending upon the Aggregate selected. It’s not possible, for example, select a Daily schedule for an Aggregate that is Monthly as the next month’s data is not complete until each month end. It’s also possible to add users to send the reports via email. The users must have access to JDE and Market Reports to be added to the “Send To” list. They will be sent an email when the scheduled report is run with a link to the newly generated report. That link will require them to login to JDE, and will validate that their Organization is correctly associated to that report before allowing them to download the file. 
* Format
Reports are delivered as CSV or Excel files. CSV formatted reports will be packaged in the form of a zip archive. Each Primary Dimension Value selected will create a single file named with the value inside that archive. Excel formatted reports will have a tab for each Primary Dimension Value selected.
* Name
This is the Name of the report. This is what will be displayed in the Report History drop down for users, and what the base name of the report file will be. All special characters will be replaced with underscores at file generation time to ensure a valid file name.

# LinkUp Support:
LinkUp provides Market Reports support Monday through Friday from 8am to 5pm CDT.
General Support
support@linkup.com 866.359.9560
Client Support
Meg Slindee
Business Development Manager meg.slindee@linkup.com 952.277.4506
www.linkup.com | 866.359.9360 | info@linkup.com | 430 N 1st Ave, Suite 790, Minneapolis, MN 55401 US


