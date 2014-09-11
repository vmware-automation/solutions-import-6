#Success
Blueprint has been successfully imported in vFabric Application Director. 

There are  few final steps you need to follow before performing this deployment.

###Prerequisites:

Download the following file and keep it in local webserver folder.

1. phpMyAdmin-3.5.2-all-languages.tar.gz: http://citylan.dl.sourceforge.net/project/phpmyadmin/phpMyAdmin/3.5.2/phpMyAdmin-3.5.2-all-languages.tar.gz

###Deployment steps:
1.Now click on deploy to deploy the application.

2.Enter name for deployment profile.

Step1: Deployment Environment tab will be displayed. Enter proper values as per your environment and click next.



Step2: Application Properties -> Service tab -> Lamp_Stack
	
		a. db_root_password : Enter the database password
	
![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/LAMP-Stack-1-7-7-Blueprint-InterraIT-50/Lamp-Stack-Property.png)
	
###Blueprint Canvas diagram for your reference: 

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/LAMP-Stack-1-7-7-Blueprint-InterraIT-50/LAMP-Stack-1.7.7-Blueprint-InterraIT-canvas.png)

###Ready to go for deployment

###Smoke test after deployment :
Verify deployment by accessing URL : http://<IP of your deployed system>/phpinfo.php

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/LAMP-Stack-1-7-7-Blueprint-InterraIT-50/Lamp-SMOKE1.png)
![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/LAMP-Stack-1-7-7-Blueprint-InterraIT-50/Lamp-php-SMOKE2.png)
![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/LAMP-Stack-1-7-7-Blueprint-InterraIT-50/Lamp-phpinfo-SMOKE3.png)
