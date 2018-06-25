For Windows & Linux
===========
Please download below softwares. 
1. apache-jmeter-4.0 
2. Apached POI 3.17

Steps To run
============
1. Source and related files in below github
https://github.com/subrazen/zycusassignment

2. Invoke Jmeter from \apache-jmeter-4.0\bin\ApacheJMeter.jar
3. In Jmeter File -> Open zycusassignement.jmx
4. In Jmeter Go to TestPlan - check the user defined variable "Path" - enter your working folder eg C://ZycusAssignment//   for linux change to linux path.
5. Update Server variable to proper server name /IP.  Refer step 7 ( use 127.0.0.1 or localhost or C:\Windows\System32\drivers\etc\host for your own servername)
6. In Jmeter click on the top node "TestPlan" and then on the right side view click browse on "Add directory or jar to classpath"  
7. Add all files unde POI lib  
	\poi-bin-3.17-20170915\poi-3.17\lib
	\poi-bin-3.17-20170915\poi-3.17\ooxml-lib

8. We need to start json-server for mock api call for Jmeter script to run.
	a. Need Nodejs installed on your system
	b. npm install json-server
	c. use db-tenantcustomers.json and db-tenantuploadfile.json to start the json-server
	
	like below
	json-server --watch db-tenantcustomers.json -p 3000
	json-server --watch db-tenantuploadfile.json -p 4000
	
Note: This is mandatory for our script to run.

9. Windows : Go to Jmeter TestPlan and run it and check the results in "View Results Tree" - all should show green.

Linux : ./jmeter.sh -n -t /path/zycusassignement.jmx

Pleas call me if any issues in running,. its running fine in my local.

