#Success
Blueprint has been successfully imported in vCloud Application Director. 

There are  few final steps you need to follow before performing the deployment.

###Prerequisites:

Download the IBM WebSphere zip and keep it in local web server folder.

###Deployment steps:
1.Now click on deploy to deploy the application.

2.Enter name for deployment profile.

Step1: Deployment Environment tab will be displayed. Enter proper values as per your environment and click next.


Step2: Application Properties -> Service tab 

		i. Clustered_WAS-Dvlp_Manager :
	
			a. im_download_url: Enter the URL to download IBM Installation Manager.
			b. ibm_username: Enter the user name for ibm download center 
			c. ibm_password: Enter the password for ibm download center
			d. admin_password: Enter the admin password
			
		ii.	Clustered_WAS-AppServer
		
			a. im_download_url: Enter the URL to download IBM Installation Manager.
			b. ibm_username: Enter the user name for ibm download center 
			c. ibm_password: Enter the password for ibm download center
			d. admin_password: Enter the admin password		


###AppServer properties for your reference:

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-6/IBM-WebSphere-App-Server-8_0-Clustered-Service/IBM-Websphere-C-Server-AppServer-Blueprint_properties.png)

###Development Manager properties for your reference:

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-6/IBM-WebSphere-App-Server-8_0-Clustered-Service/IBM-Websphere-C-Server-Development-Manager-Blueprint_properties.png)

		
###Blueprint Canvas diagram for your reference: 

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-6/IBM-WebSphere-App-Server-8_0-Clustered-Service/IBM-Websphere-Application-Server-8.0-Clustered-Service-Blueprint_Canvas.png)

###Ready to go for deployment

###Smoke Test Plan after deployment

Open the below URL in your broswer:

url = "https://${admin_ip}:50001/ibm/console/logon.jsp";

Use following credential to login

Admin User	= "$admin_username"
Admin Password	= "$admin_password"