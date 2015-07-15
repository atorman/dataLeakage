## Data Leakage Pilot - API Events

Companies continue to view data loss as a major concern. Data leakage, when left undetected, makes it difficult to identify when a specific employee removes data from Salesforce for their own purposes. The Data Leakage Detection pilot is designed so administrators can monitor and detect when users access data through the Salesforce platform. Users can access data through a programmatic interface such as the API or through a web interface like a browser.

The initial pilot of Data Leakage Detection tracks queries in near real time in the SOAP, REST, and Bulk APIs. Because greater than half of all data accessed on the platform is performed via these APIs, organizations can gain greater insights into:
* Who saw what data
* When they saw that data
* Where they accessed the data
* What fields they accessed
* How long a query took
* How many records they accessed

When combined with Login Forensics, you can also track every query back to a unique login to identify anomalies in user behavior.

Each event consists of key information about the Apex execution in the context of a limit including:

* AdditionalInfo
* ApiType
* ApiVersion
* Client
* ElapsedTime
* EventTime
* Id
* LoginHistoryId
* ObjectType
* Operation
* RowsProcessed
* Soql
* SourceIp
* UserAgent
* UserId
* Username

To learn more specifics about the Data Leakage Detection Pilot functionality, read the pilot [tip sheet](http://bit.ly/dldDocs).

## Installation

The easiest way to install this project into your org is to make use of the workbench tool (http://workbench.developerforce.com).  

1. Download a ZIP of the repository. 
2. Uncompress the files. Find the src folder with the package.xml file in it. Re-zip it on the command line: 
```zip -r deploy.zip src```
3. Open Workbench (http://workbench.developerforce.com/) 
4. Login to the desired organization with a user that has Modify All Data.  
5. Select *Deploy* from the *migration* menu and when prompted, choose your zip file and select 'Allow Missing Files' checkbox before deploying it.

## Configuration and Usage

To view the DataLeakagePage, you must assign the correct permissions to the user. An example permission set is included in this repository: Data_Leakage permission set. You should also assign the API Enabled and View Data Leakage Detection permissions on a permission set.

## Credit

Contributors include:

* Adam Torman created and orchestrated this repository
* Doug Bitting helped with the Google Charting API code

This repo is As-Is. All pull requests are welcome.

## Screen Shot
![alt tag] (https://github.com/atorman/dataLeakage/blob/master/samplePage.png)
