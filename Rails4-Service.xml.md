#Success
Blueprint has been successfully imported in your local vCloud Application Director. 

There are few final steps you need to follow before performing this deployment.

###Prerequisites:
N/A

###Deployment steps:
After importing Blueprint in vCloud Application Director, you can proceed with application deployment. The basic steps are as follows:

Step 1: Map the logical template with Cloud template (Physical Template).

Step 2: Navigate to Applications Tab and open the imported Application.

Step 3: Enter required property values appropriate to your environment:

a. Application Properties -> Service tab -> Rails4Service

      i.http_proxy : Enter the proxy URL e.g. http://x.x.x.x:portno
     ii.https_proxy: Enter the proxy URL e.g. https://x.x.x.x:portno
    iii.ftp_proxy  : Enter the proxy URL e.g. ftp://x.x.x.x:portno

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-6/Rails-4-Service-v1.0.0/Service-Property.jpg)

b. Application Properties -> Application Component -> Rails4SampleApp

      i.sample_app_port : 3001 
     ii.ruby_version    : 2.0.0
    iii.rails_version   : 4.0.0

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-6/Rails-4-Service-v1.0.0/Application-property.jpg) 

##Blueprint Canvas diagram for your reference: 

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-6/Rails-4-Service-v1.0.0/Rails-4-Service-Blueprint.jpg)
	

###Ready to go for deployment


###Smoke test after deployment:

Verify deployment by accessing URL http://WebPortal_IP:80

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-6/Rails-4-Service-v1.0.0/Smoke-test.jpg)


 








