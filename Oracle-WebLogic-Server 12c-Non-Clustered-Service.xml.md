#Success
Service has been successfully imported in your local vFabric Application Director. 

There are few final steps you need to follow before performing deployment.

###Prerequisites:

Download the  "WebLogic Server installer"(Rename the WebLogic Server installer to webLogicInstaller.bin),"demoapp.war" and  keep it in your local web server folder.


###Deployment steps:

After importing Service in Application Director, you can start using it to deploy applications. The basic steps are as follows:

Step 1:

	1. Create a new Application.
	 
    2. On the Blueprint canvas, drag and drop the supported OS template from the Logical Templates menu.

    3. From the Services menu, drag and drop this service to OS template.

    4. Save the Application.
    
Step 2: Deployment Environment tab will be displayed. Enter proper property values as per your environment and click next.

Step 3: Application Properties -> Service tab

			i. Weblogic:

				a. nfs_path: Enter the nfs path for the WebLogic Server installer
![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Oracle-WebLogic-Server-12c-Non-Clustered-Service-50/Oracle-WebLogic-Server-12c-Non-Clustered-Service-properties2.png)
			
Step 4: Application Properties -> Application Component tab

			i. DemoApp:

				a. war_file: Enter the nfs path for the demoapp.war file

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Oracle-WebLogic-Server-12c-Non-Clustered-Service-50/Oracle-WebLogic-Server-12c-Non-Clustered-Service-properties1.png)

###Blueprint Canvas diagram for your reference: 

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Oracle-WebLogic-Server-12c-Non-Clustered-Service-50/Oracle-WebLogic-Server-12c-Non-Clustered-Service-Canvas.png)

###Ready to go for deployment

###Smoke test after deployment:
	
Log into the WebLogic server console at http://<deployed IP>:7001/console/login/LoginForm.jsp
	
Log into the application at http://<deployed IP>:7001/TestWebApp/

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Oracle-WebLogic-Server-12c-Non-Clustered-Service-50/Oracle-WebLogic-Server-12c-Non-Clustered-Service-Smoke-Test.png)





 








