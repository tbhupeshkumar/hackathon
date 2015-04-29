# hackathon
Hackathon Products

Real Time Log Alert Management System - powered by LogAnalyser
-------------------------------------------------------------------------------

Files Included: 
1. logAnalyzer.zip
2. rtlams.war
3. create_log_Analyzer.sql

How to Configure "LogAnalyser"
	1. Connect to the database of your choice (If not, the download mysql or oracle and setup a database)
	2. Create a schema for logAnalyzer and execute the sql file - create_log_Analyzer.sql
	3. Copy logAnalyzer.zip to any location on the server (Unix or Windows)
    4. Unzip logAnalyzer.zip
    5. Edit logAnalyser.properties file to configure the DB URL 
    	

How To Run "LogAnalyser":
    1. Run the command - ./startLogAnalyzer.sh to start the analyzer
    2. To stop the analyzer run - ./stopLogAnalyzer.sh
    3. Log files will be generated under logAnalyzer/logs directory.

How To Deploy "Real Time Log Alert Management System" web application:
	1. Deploy the rtlams.war file onto the server of your choice.
	2. If connection pool is not available on the server, then deploy the war in explode mode 
	3. Edit rtlams.properties file to configure the database JDBC url. 



Design :
     There were multiple solutions available on the internet to gather logs, monitor logs, search logs and analyse the log. 
However, we chose to create those components on our own. 
The logAnalyser component tails the logs that are configured in the database and captures the logs statements which 
contains the KEYWORDS configured in the database. Capturing the log includes entering the details in DB for the
respective line and alert based on the configuration of the keyword, which is either EMAIL or SMS  


Real Time Analysis Results :
     The initial load test results showed the average time taken to alert for a keyword found in log to be 0.6 seconds.
      
