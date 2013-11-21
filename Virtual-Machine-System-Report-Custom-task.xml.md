#Success
Blueprint has been successfully imported in vFabric Application Director. 

There are  few final steps you need to follow before performing this deployment.

###Prerequisites:

None
###Deployment steps:
1.Now click on deploy to deploy the application.

2.Enter name for deployment profile.

Step1: Deployment Environment tab will be displayed. Enter proper values as per your environment and click next.


Step2: Drag and drop Virtual Machine System Report Task just after the Application 


![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Virtual-Machine-System-Report-50/VMSystemReport1.png)

		
###Blueprint Canvas diagram for your reference: 

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Virtual-Machine-System-Report-50/VMSystemReport3.png)

###Ready to go for deployment

###Smoke Test Plan

Create JDBC connection to access the DB. URL to be used:
String url = "jdbc:db2://<db_machine_ip>:50000/<db_name>";





 








