#Success
Blueprint has been successfully imported in vFabric Application Director. 

There are  few final steps you need to follow before performing this deployment.

###Prerequisites:

Download the following files and keep it in local web server folder:

	1. liferay-portal-tomcat-6.1.0-ce-ga1-20120106155615760.zip
	2. Share.war
	3. mysql-connector-java-5.0.8.tar.gz

###Deployment steps:
1.Now click on deploy to deploy the application.

2.Enter name for deployment profile.

Step1: Deployment Environment tab will be displayed. Enter proper values as per your environment and click next.


Step2: Application Properties -> Service tab -> OpenLDAP	
	
 			i. rootpw: root password

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Liferay-OpenLDAP-Application-Blueprint-50/Service-property-OpenLdap.png) 

Step3: Application Properties -> Service tab -> Liferay

	
	i. mysql_connector: Enter the path for  *mysql-connector-java-5.0.8.tar.gz

    ii.installer_url: Enter the path for liferay-portal-tomcat-6.1.0-ce-ga1-20120106155615760.zip

    iii.alfresco_share_war_url:Enter the path for share.war 


![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Liferay-OpenLDAP-Application-Blueprint-50/Service-property-Liferay.png)
	
##Blueprint Canvas diagram for your reference: 

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Liferay-OpenLDAP-Application-Blueprint-50/Liferay-OpenLDAP-Application-Blueprint-Canvas.png)

###Ready to go for deployment

###Smoke test after deployment:

Verify deployment by accessing URL http://WebPortal_IP:8080/

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Liferay-OpenLDAP-Application-Blueprint-50/Smoke-Test.png)






 








