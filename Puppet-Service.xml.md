#Success
Service with sample blueprint have been successfully imported in vFabric Application Director. 

Sample Blueprint is with Service and one of the supported operating system. User can use any of supported Operating Systems listed in Service. 

There are few final steps you need to follow before performing deployment.

###Prerequisites:

Download the puppet/Puppet Enterprise package for the corresponding Operating System and keep it in  local web server folder. Example: puppet-enterprise-2.5.3-el-5-x86_64.tar.gz for Ubuntu 32 bit (10.4).

puppet : https://pm.puppetlabs.com/puppet-enterprise 

###Deployment steps:

After importing Blueprint in vFabric Application Director, you can proceed with application deployment. The basic steps are as follows:

Step 1: Map the logical template with Cloud  template (Physical Template).

Step 2: Navigate to Applications Tab and open the imported Application.

Step 3: Enter required property values appropriate to your environment.

		a. Application Properties -> Service tab ->Puppet_Enterprise

			a. agent_cert: Enter the systems certificate name
			b. installer_payload: Enter the appropriate package for the operating system (Path of Operating system webs server)
			c. puppet server: Enter appropriate puppet master name
			

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Puppet-Service-50/Puppet-Service-properties.png)
	
Step 4: Save the Application and proceed for deployment.

###Blueprint Canvas diagram for your reference: 

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Puppet-Service-50/Puppet-Service-Canvas.png)

###Ready to go for deployment




 








