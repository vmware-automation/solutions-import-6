#Success
Service with sample blueprint have been successfully imported in vFabric Application Director. 

Sample Blueprint is with Service and one of the supported operating system. User can use any of supported Operating Systems listed in Service. 

There are few final steps you need to follow before performing deployment.


###Prerequisites:

Download the following files and keep it in local web server folder:
	
	1. Alfresco_enterprise-4.0.1_installer.bin
	
###Deployment steps:

After importing Blueprint in vFabric Application Director, you can proceed with application deployment. The basic steps are as follows:

Step 1: Map the logical template with Cloud  template (Physical Template).

Step 2: Navigate to Applications Tab and open the imported Application.

Step 3: Enter required property values appropriate to your environment:

	a. Application Properties -> Service tab ->Alfresco
	
        i.installer_url: Enter URL for Alfresco application installation
	
       ii.alfresco_admin_password : Enter the password for alfresco application login
	 
	
![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Alfresco-Service-50/Service-Property-new.jpg) 

##Blueprint Canvas diagram for your reference: 

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Alfresco-Service-50/Blueprint1-new1.jpg)

###Ready to go for deployment

###Smoke test after deployment:

Verify deployment by accessing URL: http://< WebPortal IP >:8080/alfresco 

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Alfresco-Service-50/Smoke-Test.png)
