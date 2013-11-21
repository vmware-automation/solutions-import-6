#Success
Service with sample blueprint have been successfully imported in vFabric Application Director. 

Sample Blueprint is with Service and one of the supported operating system. User can use any of supported Operating Systems listed in Service. 

There are few final steps you need to follow before performing deployment.


###Prerequisites:

None

###Deployment steps:

After importing Blueprint in vFabric Application Director, you can proceed with application deployment. The basic steps are as follows:

Step 1: Map the logical template with Cloud  template (Physical Template).
Step 2: Navigate to Applications Tab and open the imported Application.

Step 3: Enter required property values appropriate to your environment.

		a. Application Properties -> Service tab ->Sumo_Logic_Collector

			a. EMAIL: Enter the Sumo Logic account email address
			b. PASSWORD: Enter the Sumo Logic account password
			c. NAME: Enter the name used for your collector (Optional)  

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Sumo-Service-50/Sumo-Service-proeprties.png)
 	
Step 4: Save the Application and proceed for deployment

###Blueprint Canvas diagram for your reference: 

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Sumo-Service-50/Sumo-Service-canvas.png)

###Ready to go for deployment


 








