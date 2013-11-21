#Success
Blueprint has been successfully imported in vFabric Application Director. 

There are few final steps you need to follow before performing this deployment.

###Prerequisites:

None
###Deployment steps:

1.Now click on deploy to deploy the application.

2.Enter name for deployment profile.

  Step 1: Deployment Environment tab will be displayed. Enter proper values as per your environment and click next.


Step2: Application Properties -> Service tab 

	i. Application Properties -> Service tab -> Lamp_Stack
	
		a. db_root_password : Enter the database root Password 
        b. phpMyAdmin_url   : Enter the path of phpMyAdmin Application 

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Piwik-1_8_2-Linux-Blueprint-InterraIT-50/Service-Property-Lamp-stack.png) 
                      
	ii. Application Properties -> Service tab -> piwik-2  
	
		a. piwik_username: Enter piwik username 
        b. piwik_password: Enter piwik password


![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Piwik-1_8_2-Linux-Blueprint-InterraIT-50/Service-Property-Piwik.png)


###Blueprint Canvas diagram for your reference: 

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Piwik-1_8_2-Linux-Blueprint-InterraIT-50/Piwik-1.8.2-on-Linux-Blueprint-InterraIT-canvas.png)

###Ready to go for deployment.


###Smoke test after deployment:

Verify deployment by accessing URL http://{ip:port}/piwik

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Piwik-1_8_2-Linux-Blueprint-InterraIT-50/Smoke-Test.png)




 












 








