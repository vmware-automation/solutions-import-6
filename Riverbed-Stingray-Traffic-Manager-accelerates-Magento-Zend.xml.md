#Success
Blueprint has been successfully imported in your local vFabric Application Director. 

There are  few final steps you need to follow before performing this deployment.

###Prerequisites:

Download following software from the following link and keep it in your local web server folder.

1. **Stingray Traffic Manager Version 9.3 (32-bit)**:
    https://support.riverbed.com/download.htm?sid=jvrmms6hm502u6jv11ij9vk92s


2. **Stingray Traffic Manager Version 9.3 (64-bit) :**
    https://support.riverbed.com/download.htm?sid=qbr1k45ualc3gijn0qavnjaei7 
    
3.  **Zend Server Version 9.3:**
    http://downloads.zend.com/zendserver/5.6.0/ZendServer-5.6.0-   
      RepositoryInstaller-linux.tar.gz

4.  **MySQL Database Server:**
    http://downloads.zend.com/zendserver/5.6.0/ZendServer-5.6.0-   
      RepositoryInstaller-linux.tar.gz

5.  **Zend Trial License:**
     http://www.zend.com/products/server/license
  
###Deployment steps:

1. Click on deploy to deploy the application.

2. Enter name for deployment profile.

Step 1: Deployment Environment tab will be displayed. Enter proper values       as per your environment and click next 

Step2: Application Properties -> Service tab
 
      i. Application Properties -> Service tab -> Zend_Server_PHP_Cluster_Manager_Service

      a. zend api key name    : Enter the api key name
      b. zend api key         : Enter the encrypted key value
      c. zend order number    : Enter the Trial license order number
      d. db_root_password     : Enter the Mysql database root password
      e. zscm db password     : Enter the password for zscm database
      f. zscm node ui password: Enter the password to access zscm  application
      g. zendmanager ui password: Enter the password to access zendmanager application 
      h. zend license key         : Enter the zend license key 
      i. zendmanager license key  : Enter the zendmanager license key
      j. zendmanager order number : Enter the zendmanager trial license order number
      
![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Riverbed-Stingray-Traffic-Manager-accelerates-Magento-50/Zend-Server-PHP-Cluster-Manager-Service.jpg)

      ii. Application Properties -> Service tab -> Zend_Server_PHP_Application_Server

      a. zend order number    : Enter the Trial license order number
      b. zend license key     : Enter the zend license key
      c. zend api key name    : Enter the api key name
      d. zend api key         : Enter the encrypted key value
      e. zend node ui password: Enter the password to access zend  
           
![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Riverbed-Stingray-Traffic-Manager-accelerates-Magento-50/Zend-Server-PHP-Cluster-Application-Manager-Service.jpg)
    
     iii. Application Properties -> Service tab -> Mysql 
      a. db_root_password      : Enter the Mysql database root password 
![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Riverbed-Stingray-Traffic-Manager-accelerates-Magento-50/Stingray-Traffic-Manager-Accelerates-Magento-MySQL-Property.jpg)    
     
     iv. Application Properties -> Service tab -> Stingray Traffic Manager accelerates magento
      a. Stingray download URL : Enter the URL to download stingray software
![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Riverbed-Stingray-Traffic-Manager-accelerates-Magento-50/Stingray-Traffic-Manager-Accelerates-Magento-Service.jpg)
Step3: Application Properties -> Application Component 

     i. Application Properties -> Application Component -> init_magento_db 
      a.magento_db_password    : Enter the password to access magento Database
![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Riverbed-Stingray-Traffic-Manager-accelerates-Magento-50/Stingray-Traffic-Manager-Accelerates-Magento-Application-Property-init-magento-db.jpg)
    ii.Application Properties -> Application Component -> Magento
      a.magento_admin_password : Enter the password to access magento Ecommerce Portal 

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Riverbed-Stingray-Traffic-Manager-accelerates-Magento-50/Stingray-Traffic-Manager-Accelerates-Magento-Application-Property-Magento-DB.jpg)
	
###Blueprint Canvas diagram for your reference: 

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Riverbed-Stingray-Traffic-Manager-accelerates-Magento-50/Stingray-Traffic-Manager-Accelerates-Magento-Canvas.jpg)

###Ready to go for deployment

### Smoke Test

Verify deployment by accessing of Magento IP URL:  http://Zend_Appnode_1_IP:80/index.php/

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Riverbed-Stingray-Traffic-Manager-accelerates-Magento-50/Smoke-test-Magento-Admin-Panel.jpg)

![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Riverbed-Stingray-Traffic-Manager-accelerates-Magento-50/Smoke-test-Magento-Website.jpg)

Verify deployment by accessing of Stingray Traffic Managers Instance IP URL:  http://:<Stingray Traffic Managers Instance IP>8080/index.php/
![alt tag](https://raw.github.com/vmware-applicationdirector/solutions-import-beta/Riverbed-Stingray-Traffic-Manager-accelerates-Magento-50/Smoke-test-Stingray-Admin-Console.jpg)



 

 



