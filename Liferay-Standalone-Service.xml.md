#Success
Blueprint has been successfully imported in  vFabric Application Director. 

There are  few final steps you need to follow before performing this deployment.

###Prerequisites:
Download the following  files and keep them in local web server folder.

1. mysql-connector-java-5.0.8.tar.gz
2. liferay-portal-tomcat-6.1.1-ce-ga2-20120731132656558.zip
3. Share.war

###Deployment steps:
1.Now click on deploy to deploy the application.

2.Enter name for deployment profile.

Step1: Deployment Environment tab will be displayed. Enter proper values as per your environment and click next.


Step2: Application Properties -> Node tab

	    a. Memory (MB) : Enter numerical value as 2044   
            b. vCPU        : Enter numerical value as 1  

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Liferay-Standalone-Service-50/Node-property.png)
   		
Step3: Application Properties -> Service tab 

	i. Application Properties -> Service tab -> Liferay_Standalone  
		
        a. mysql_connector: Enter the path for mysql-connector-java-5.0.8.tar.gz
        b. installer_url  : Enter the path for Liferay application(liferay-portal-tomcat-6.1.1-ce-ga2-20120731132656558.zip)         
        c. alfresco_share_war_url: Enter the tomcat server path for alfresco web archiver deployment  

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Liferay-Standalone-Service-50/Service-property-Liferay-Standalone.png)

###Blueprint Canvas diagram for your reference: 

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Liferay-Standalone-Service-50/Liferay-Standalone-Service-canvas.png)

###Ready to go for deployment

### Smoke Test after deployment :

Verify deployment by accessing URL  http://WebPortal_IP:8080/

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Liferay-Standalone-Service-50/Smoke-Test.jpg)




 








