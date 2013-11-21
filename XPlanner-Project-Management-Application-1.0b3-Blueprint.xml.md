#Success
Blueprint has been successfully imported in vFabric Application Director. 

There are  few final steps you need to follow before performing this deployment.

###Prerequisites:

Download the following file and keep it in local web server folder.

1. Xplanner-plus.war

###Deployment steps:
1.Now click on deploy to deploy the application.

2.Enter name for deployment profile.

Step1: Deployment Environment tab will be displayed. Enter proper values as per your environment and click next.

Step2: Application Properties -> Service tab -> Preinstalled_MySql_server

			a. db_root_password : Enter the Database password 

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/XPlanner-Project-Mgmt-Appl-1_0-b3-Blueprint-50/Service-Property-Mysql.png)

		ii. Application Properties -> Service tab -> Apache

			No changes in properties value

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/XPlanner-Project-Mgmt-Appl-1_0-b3-Blueprint-50/Service-Property-Apache.png)
    	
       ii. Application Properties -> Service tab -> vFabric_tc_Server

	    a. install_path : Enter the installation directory path for tcserver 
	    b. jobsh        : Enter the path of job.sh file 
	    c. nfs_path		: Enter the path of tc server
	    d. war          : Enter the path of war 

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/XPlanner-Project-Mgmt-Appl-1_0-b3-Blueprint-50/Service-Property-Vfabric-tc-Server.png)
    
Step3: Application Properties
		
		i. XPlanner_Webapp :	 
	
    	        war_file : Enter path of "xplanner-plus.war" file 
    	        
![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/XPlanner-Project-Mgmt-Appl-1_0-b3-Blueprint-50/Application-Component-Property-Xplanner-Webapp.png)    	        

   	    ii. Application Properties -> Application tab -> xplanner_db 

              xplanner_db_pass : Enter the xplanner database password  

	
![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/XPlanner-Project-Mgmt-Appl-1_0-b3-Blueprint-50/Application-Component-Property-xplanner-db.png)
	
###Blueprint Canvas diagram for your reference: 

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/XPlanner-Project-Mgmt-Appl-1_0-b3-Blueprint-50/Blueprint-Canvas.png)

###Ready to go for deployment

###Smoke test after deployment:

Verify deployment by accessing URL http://WebPortal_IP:8081/
![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/XPlanner-Project-Mgmt-Appl-1_0-b3-Blueprint-50/Smoke-Test.png)




 








