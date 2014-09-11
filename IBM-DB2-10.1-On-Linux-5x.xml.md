#Success
Blueprint has been successfully imported in vFabric Application Director. 

There are  few final steps you need to follow before performing the deployment.

###Prerequisites:

Download the IBM DB2 tar ball and keep it in local web server folder.

###Deployment steps:
1.Now click on deploy to deploy the application.

2.Enter name for deployment profile.

Step1: Deployment Environment tab will be displayed. Enter proper values as per your environment and click next.


Step2: Application Properties -> Service tab 

		i. DB2:
	
			a. download_url: Enter the url to download the DB2 tar ball
			b. database_password: Enter the database password
			c. instance_password: Enter the password of the DB2 instance name

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/IBM-DB2-10_1-Linux-Blueprint-50/IBM-DB2-10.1-On-Linux-Blueprint_properties.jpg)

		
###Blueprint Canvas diagram for your reference: 

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/IBM-DB2-10_1-Linux-Blueprint-50/IBM-DB2-10.1-On-Linux-Blueprint_Canvas.jpg)

###Ready to go for deployment

###Smoke Test Plan after deployment

Create JDBC connection to access the DB. URL to be used:

String url = "jdbc:db2://<db_machine_ip>:50000/<db_name>";







 








