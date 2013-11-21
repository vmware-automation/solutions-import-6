#Success
Service with sample blueprint have been successfully imported in vFabric Application Director. 

Sample Blueprint is with Service and one of the supported operating system. User can use any of supported Operating Systems listed in Service. 

There are few final steps you need to follow before performing deployment.

###Prerequisites:

Download the following file and keep it in  local web Server folder.

1. jboss-as-7.1.0.Final.zip 

###Deployment steps:
After importing Blueprint in vFabric Application Director, you can proceed with application deployment. The basic steps are as follows:

Step 1: Map the logical template with Cloud  template (Physical Template).

Step 2: Navigate to Applications Tab and open the imported Application.

Step 3: Enter required property values appropriate to your environment.

      a. Application Properties -> Service tab -> JBoss _ Application _ Server_7

           	 i) zip_url: Enter the URL to download the zip file 
          
             ii) JBOSS_MGMT_USER: Enter Jboss Management user(admin)  
         
             iii)JBOSS_MGMT_PWD: Enter Jboss password

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/JBoss-Application-Server7-Service-50/Service-Property-Jboss.png)

Step 4: Save the Application and proceed for deployment

###Blueprint Canvas diagram for your reference: 

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/JBoss-Application-Server7-Service-50/JBoss-Application-Server7-Service-Blueprint-Canvas.png)

###Ready to go for deployment

###Smoke test after deployment:

Verify deployment by accessing URL http://< WebPortal IP >:8080/

click on "Administrative Console"

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/JBoss-Application-Server7-Service-50/Smoke-test-Login-page.png)

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/JBoss-Application-Server7-Service-50/Smoke-test-Index-page.png)









 








