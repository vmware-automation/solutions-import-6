#Success
Blueprint has been successfully imported in vFabric Application Director. 

There are  few final steps you need to follow before performing this deployment.

###Prerequisites:

Download the following files and keep it in local web server folder.
1. wso2esb-4.0.3.zip
2. apache-ant-1.8.4-bin.tar.gz

###Deployment steps:
1.Now click on deploy to deploy the application.

2.Enter name for deployment profile.

Step1: Deployment Environment tab will be displayed. Enter proper values as per your environment and click next.

Step2: Application Properties -> Service tab

		i. :WSO2_Enterprise_Service_Bus:
	
			a. wso2_esb_download_url: Enter the path for wso2esb-4.0.3.zip
			b. ant_download_url: Enter the path for apache-ant-1.8.4-bin.tar.gz

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/WSO2-ESB-4_0_3_Linux-Blueprint-50/WSO2-ESB-4.0.3-for-Linux-Blueprint-by-InterraIT_properties.jpg)

###Blueprint Canvas diagram for your reference: 

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/WSO2-ESB-4_0_3_Linux-Blueprint-50/WSO2-ESB-4.0.3-for-Linux-Blueprint-by-InterraIT_Canvas.png)

###Ready to go for deployment.

###Smoke test after deployment :

Verify deployment by accessing URL http://WSO2_ESB_Machine_ip:port







 








