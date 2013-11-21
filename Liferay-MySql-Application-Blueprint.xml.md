#Success
Blueprint has been successfully imported in  vFabric Application Director. 

There are  few final steps you need to follow before performing this deployment.

###Prerequisites:

Download the  following files and keep it in local web server folder.
 
	1. liferay-portal-tomcat-6.1.1-ce-ga2-20120731132656558.zip
	2. Share.war
	3. mysql-connector-java-5.0.8.tar.gz
   

###Deployment steps:
1.Now click on deploy to deploy the application.

2.Enter name for deployment profile.

Step1: Deployment Environment tab will be displayed. Enter proper values as per your environment and click next.


Step2: Application Properties -> Service tab

		i. Application Properties -> Service tab -> Liferay
	
			a. mysql_connector: Enter the local web server path of mysql_connector_java_tar.gz 
            b. installer_url: Enter the local web server path of Liferay portal application    
            c. alfresco_share_war_url: Enter the local web server path of alfresco web archiver deployment  


![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Liferay-MySql-Application-Blueprint-50/Service_property_Liferay.png)

		
		ii. Application Properties -> Service tab -> MySQL  
	
		a. db_root_password: Enter database root password 
        
![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Liferay-MySql-Application-Blueprint-50/Service_property_Mysql.png)
	
###Blueprint Canvas diagram for your reference: 

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Liferay-MySql-Application-Blueprint-50/Liferay-MySql-Application-Blueprint-Canvas.png)

###Ready to go for deployment

###Smoke test after deployment:

Verify deployment by accessing URL http://WebPortal_IP:8080/

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Liferay-MySql-Application-Blueprint-50/Smoke%20Test.png)



