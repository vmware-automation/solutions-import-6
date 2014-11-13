#Success
Blueprint has been successfully imported in vRealize Automation Application Services. 

There are  few final steps you need to follow before performing this deployment.

###Setup External Service Instances:

Create three "External Service Instances" in your Deployment Environment.  One External Service Instance is required per type of external instance.  

This blueprint only uses three of the four available (the fourth is a "User-Provided Service" and is not needed for this blueprint).

See the example below.  If the "space" property value is available for the External Service Instance, please provide your Cloud Foundry space.  See the example below.

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-6/Spring-Trader-BP-v1.0.0/screen1.png)

	
###Update Credentials:

Open the blueprint, click on the "Endpoint" node, and update the credentials to contain your Cloud Foundry credentials.  See example below.

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-6/Spring-Trader-BP-v1.0.0/screen2.png)

###Ready to go for deployment



 








