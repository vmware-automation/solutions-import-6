#Success
Service has been successfully imported in your local vFabric Application Director. 

There are few final steps you need to follow before performing deployment.

###Prerequisites:

download Riverbed Stingray Traffic Manager developer edition from https://support.riverbed.com/software/stingray/trafficmanager.htm and and keep it in your local webserver folder.

###Deployment steps:

After importing Service in Application Director, you can start using it to deploy applications. The basic steps are as follows:

Step 1:

	1. Create a new Application.
	 
    2. On the Blueprint canvas, drag and drop the supported OS template from the Logical Templates menu.

    3. From the Services menu, drag and drop this service to OS template.

    4. Save the Application.
    
Step 2: Deployment Environment tab will be displayed. Enter proper property values as per your environment and click next.

Step 3: Application Properties -> Service tab ->Riverbed_Stingray_Traffic_Manager_9.0

			a. Stingray_Download_URL: Enter the URL to download the Stingray Software
			b. Stingray_Node_IPs: Enter the IP addresses of Backend Nodes
![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Riverbed-Stingray-Traffic-Manager-9_0-Service-50/Riverbed-Stingray-Traffic-Manager-9.0_properties.jpg)  
	
##Blueprint Canvas diagram for your reference: 

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Riverbed-Stingray-Traffic-Manager-9_0-Service-50/Riverbed-Stingray-Traffic-Manager-9.0-Canvas.jpg)


##Ready to go for deployment




 








