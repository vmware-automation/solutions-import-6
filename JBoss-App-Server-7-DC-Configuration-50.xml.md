#Success
Blueprint has been successfully imported in your local vFabric Application Director. 

There are  few final steps you need to follow before performing this deployment

###Prerequisites:

Download following software from the following link and keep it in your local web server folder.

1. jboss-as-7.2.0.Final.tar.gz
2. domain-master.xml
3. host-master.xml
4. host-slave.xml
5. jboss-as-domain-slave.sh
6. common_utils

###Deployment steps:
1. Click on deploy to deploy the application.

2. Enter name for deployment profile.

Step 1: Deployment Environment tab will be displayed. Enter proper values       as per your environment and click next 

Step2: Application Properties -> Service tab
 
   i. Application Properties -> Service tab -> JBoss_7_Slave_Instance

     a. zip_url : Enter the path of  jboss-as-7.2.0.Final.tar.gz
	 b. domain_init_script : Enter the path of jboss-as-domain-slave.sh
	 c. host_slave :Enter the path of host-slave.xml

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/JBoss-App-Server-7-DC-Configuration-50/JBoss-App-Server-7-DC-Configuration-slave1-properties.png)
  
  ii. Application Properties -> Service tab -> JBoss_7_Slave_Instance-2

     a. zip_url : Enter the path of  jboss-as-7.2.0.Final.tar.gz
	 b. domain_init_script : Enter the path of jboss-as-domain-slave.sh
	 c. host_slave :Enter the path of host-slave.xml
 
![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/JBoss-App-Server-7-DC-Configuration-50/JBoss-App-Server-7-DC-Configuration-slave2-properties.png)
	  
  iii.  Application Properties -> Service tab ->JBoss_7_Domain_Controller

	 a. common_utils : Enter the path of common_utils
	 b. domain_init_script : Enter the path of jboss-as-domain-slave.sh
	 c. domain_master : Enter the path of domain-master.xml
	 d. host_master : Enter the path of host-master.xml
	 e. zip_url : Enter the path of  jboss-as-7.2.0.Final.tar.gz
	 f. master_cluster_password : Enter the master cluster password
![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/JBoss-App-Server-7-DC-Configuration-50/JBoss-App-Server-7-DC-Configuration-dc-properties.png)
###Blueprint Canvas diagram for your reference: 

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/JBoss-App-Server-7-DC-Configuration-50/JBoss-App-Server-7-DC-Configuration-blueprint-canvas.png)

###Ready to go for deployment


###Smoke Test after deployment:

1) Verify deployment by accessing URL: 
http://<domain controller ip>:9990/console

2) From the CLI(Login to DC or slave1 or slvae 2)

[root@JBoss7-BDULH8AK bin]# $JBOSS_HOME/bin/jboss-cli.sh --controller=<Domain Controller IP>
You are disconnected at the moment. Type 'connect' to connect to the server or 'help' for the list of supported commands.
[disconnected /] connect

[domain@<Domain Controller IP>/] ls -l /host

master

slave1

slave2

[domain@<Domain Controller IP /] 



 








