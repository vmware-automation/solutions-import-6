#Success
Blueprint has been successfully imported in  vFabric Application Director. 

There are  few final steps you need to follow before performing this deployment.

###Prerequisites:

Download  the following files and keep them in local web server folder.

		
	1. Alfresco_enterprise-4.1.5_installer.bin
	2. Share.war
	3. mysql-connector-java-5.0.8.tar.gz
	4. liferay-portal-tomcat-6.1.1-ce-ga2-20120731132656558.zip
    
###Deployment steps:
1.Now click on deploy to deploy the application.

2.Enter name for deployment profile.

Step 1: Deployment Environment tab will be displayed. Enter proper values as per your environment and click next.


Step 2: Application Properties -> Service tab 

	i. Application Properties -> Service tab -> Alfresco
		
        a. installer_url: Enter the local web server path of install Alfresco application  
        b. mysql_connector: Enter the local web server path of mysql-connector-java.tar.gz
        c. alfresco_admin_password: Enter the alfresco admin password 


![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Liferay-Alfresco-Application-Blueprint-50/Service-property-Alfresco.png)

		
	ii. Application Properties -> Service tab -> Liferay 
	
		a. mysql_connector: Enter the local web server path of mysql-connector-java.tar.gz
        b. installer_url  : Enter the local web server path of Liferay application         
        c. alfresco_share_war_url: Enter the tomcat server path for alfresco web archiver deployment(share.war)

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Liferay-Alfresco-Application-Blueprint-50/Service-property-Liferay.png)
	
###Blueprint Canvas diagram for your reference:

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Liferay-Alfresco-Application-Blueprint-50/Service-property-Alfresco.png) 


###Ready to go for deployment

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Liferay-Alfresco-Application-Blueprint-50/Liferay-Alfresco-Application-Blueprint-Canvas.png)


###Smoke test after deployment:

Verify deployment by accessing URL http://WebPortal_IP:8080/

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Liferay-Alfresco-Application-Blueprint-50/Smoke-Test.png)





 








