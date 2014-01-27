#Success
Blueprint has been successfully imported in  vCloud Application Director. 

There are few final steps you need to follow before performing this deployment.

###Prerequisites:

Download the follwing files and and keep it in local web server folder.

	1. alfresco-enterprise-4.0.1-installer-linux-x64.bin
	2. mysql-connector-java-5.0.8.tar.gz


###Deployment steps:
1.Now click on deploy to deploy the application.

2.Enter name for deployment profile.

Step1: Deployment Environment tab will be displayed. Enter proper values as per your environment and click next.


Step2: Application Properties -> Service tab 

	i. Application Properties -> Service tab -> Alfresco
	
		a. mysql_connector: Enter the path of NFS server where mysql-connector-java-5.0.8.tar.gz file is located 
		b. installer_url: Enter the installer URL to install Alfresco Enterprise application    
		c. alfresco_admin_password: Enter the password 

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-6/Alfresco-MySql-App-BP-V1.0.0/Service-Property-Alfresco.png)
             
	ii. Application Properties -> Service tab -> MySQL  
	
		a. db_root_username: Enter database username 
		b. db_root_password: Enter database password

        
![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-6/Alfresco-MySql-App-BP-V1.0.0/Service-Property-MySql.png)
				
	
###Blueprint Canvas diagram for your reference: 

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-6/Alfresco-MySql-App-BP-V1.0.0/Blueprint-Canvas.png)

###Ready to go for deployment


###Smoke test after deployment:

Verify deployment by accessing URL http://WebPortal_IP:8080/alfresco

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-6/Alfresco-MySql-App-BP-V1.0.0/Smoke-Test.png)




 








