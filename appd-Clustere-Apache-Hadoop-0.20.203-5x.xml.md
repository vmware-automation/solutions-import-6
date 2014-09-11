#Success
Blueprint has been successfully imported in vFabric Application Director. 

There are  few final steps you need to follow before performing this deployment.

###Prerequisites:

Download the "HadoopDemoApp.war" and "job.sh" files form following links and keep in local web server folder.

https://github.com/vmware-applicationdirector/solutions-import-beta/tree/appd-Clustere-Apache-Hadoop-50-blueprint

###Deployment steps:
1.Now click on deploy to deploy the application.

2.Enter name for deployment profile.

Step1: Deployment Environment tab will be displayed. Enter proper values as per your environment and click next.


Step2: Application Properties -> Service tab

		i. Hadoop_NameNode:
	
			a. password: Enter the password for Hadoop user

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/appd-Clustere-Apache-Hadoop-50-blueprint/AfterDeployment-Step1.jpg)

		
		ii. vFabric_tc_Server_SYSTEM:
	
			a. jobsh: Local webserver path where you kept "job.sh" file 
		
			b. nfs_path: Path of nfs server
		
			c. war: Local webserver path where you kept "HadoopDemoApp.war" file
	
![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/appd-Clustere-Apache-Hadoop-50-blueprint/AfterDeployment-Step2.jpg)
	
###Blueprint Canvas diagram for your reference: 

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/appd-Clustere-Apache-Hadoop-50-blueprint/Hadoop-Canvas-Diagram.png)

###Ready to go for deployment







 








