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

Step1: Deployment Environment tab will be displayed. Enter proper values as per your environment and click next.


Step2: Application Properties -> Service tab -> OpenLDAP

	i. rootpw: Enter OpenLDAP root password

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Liferay-OpenLDAP-MySql-Alfresco-App-Blueprint-50/Service-property-OpenLdap.png) 

Step3: Application Properties -> Service tab -> MYSQL
	
	i. db_root_password: Enter the database root password

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Liferay-OpenLDAP-MySql-Alfresco-App-Blueprint-50/Service-property-Mysql.png) 
	    
	    
Step4: Application Properties -> Service tab -> Liferay

	    i. mysql_connector: Enter path of  mysql-connector-java-5.0.8.tar.gz for MySql connectivity with tomcat application server 
	
	    ii.installer_url: Enter path for liferay-portal-tomcat application (liferay-portal-tomcat-6.1.1-ce-ga2-20120731132656558.zip)
	
	    iii.alfresco_share_war_url: Enter path for  Share.war
	    
![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Liferay-OpenLDAP-MySql-Alfresco-App-Blueprint-50/Service-property-Liferay.png) 
	    
Step5: Application Properties -> Service tab -> Alfresco

	    i. installer_url : Enter path of Alfresco_enterprise-4.1.5_installer.bin
	    ii. mysql_connector: Enter path of  mysql-connector-java-5.0.8.tar.gz
	    iii. alfresco_admin_password: Enter alfresco admin password 

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Liferay-OpenLDAP-MySql-Alfresco-App-Blueprint-50/Service-property-Alfresco.png)
	
##Blueprint Canvas diagram for your reference: 

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Liferay-OpenLDAP-MySql-Alfresco-App-Blueprint-50/Blueprint-Canvas.png)

###Ready to go for deployment

###Smoke Test after deployment

Verify deployment by accessing URL : http://< WebPortal IP >:8080/

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Liferay-OpenLDAP-MySql-Alfresco-App-Blueprint-50/Smoke-test.png)



 








