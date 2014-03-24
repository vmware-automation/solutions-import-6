#Success
Congratulations! The blueprint has been successfully imported in vCloud Application Director.

There are  few final steps you need to follow before performing this deployment.

###Prerequisites:

1. Expect package requirement
The WebLogic domain configuration utility requires the expect package for automation. Therefore, you need to ensure that your VM has expect installed and available in the PATH. You can either install the package in your OS template or you can provide a command or script in the CUSTOM_SCRIPT property of the Bootstrap service. For example, I use the following property value: yum install expect.x64.

2. Oracle installer files
Upload the Oracle installer files to the artifacts sub-directory on the Application Director server. Create a sub-directory called trymaran and stash all the installer files there. Please see below for the list of files that I use.

$ ls /opt/vmware/darwin/htdocs/artifacts/trymaran/
jdk-6u45-linux-amd64.rpm
jdk-6u45-linux-x64.bin
ofm_osb_generic_11.1.1.7.0_disk1_1of1.zip
ofm_rcu_linux_11.1.1.7.0_64_disk1_1of1.zip
ofm_soa_generic_11.1.1.7.0_disk1_1of2.zip
ofm_soa_generic_11.1.1.7.0_disk1_2of2.zip
wls1036_generic.jar

For your convenience, I have listed the URL below where you can download the Oracle installer files from. You will need an Oracle.com login and password to access the software. If you don't have one, you may register for free at the same login page. Download these files to the local AppD server under the directory shown above.

2.1 JDK (file: jdk-6u45-linux-x64.bin)
http://download.oracle.com/otn/java/jdk/6u45-b06/jdk-6u45-linux-x64.bin

2.2 Oracle Service Bus software (file: ofm_osb_generic_11.1.1.7.0_disk1_1of1.zip)
http://download.oracle.com/otn/nt/middleware/11g/111170/ofm_osb_generic_11.1.1.7.0_disk1_1of1.zip

2.3 Repository Creation Utility (file: ofm_rcu_linux_11.1.1.7.0_64_disk1_1of1.zip)
http://download.oracle.com/otn/linux/middleware/11g/111170/ofm_rcu_linux_11.1.1.7.0_64_disk1_1of1.zip

2.4 SOA Suite (files: ofm_soa_generic_11.1.1.7.0_disk1_*of2.zip)
http://download.oracle.com/otn/nt/middleware/11g/111170/ofm_soa_generic_11.1.1.7.0_disk1_1of2.zip
http://download.oracle.com/otn/nt/middleware/11g/111170/ofm_soa_generic_11.1.1.7.0_disk1_2of2.zip

2.5 WebLogic Server (file: wls1036_generic.jar)
http://download.oracle.com/otn/linux/middleware/11g/wls/1036/wls1036_generic.jar


###Deployment steps:

This section contains details of the required properties which you need to fill in. Most of the required properties have sensible defaults, and you will not need to alter them if you're satisfied with the default value. This section is meant to give you more information about the most important properties.

1 *:global_conf (default: https://${darwin.server.ip}:8443/darwin/conf/darwin_global.conf)
The global configuration file. This script is run before every task, so it's a great place to put global settings such as HTTP proxy, set environment variables, etc.

2 *:ENABLED (default: true for most components)
All optional components have an ENABLED property which can be set to false if you don't want to install it.

3 *:DELETE_CONTENT (default: false)
When set to true, the service will delete the large downloaded installer files after the installation is successful, thereby saving disk space.

4 *:MW_HOME (default: /oracle/middleware)
Oracle middleware home under which all middleware components will be installed.

5 *:OS_USER (default: oracle)
OS user to run the Oracle installation package. This user must already exist. Note that Oracle does not allow root to run the installation.

6 *:TMP_DIR (default: /tmp)
Temporary directory in which to unzip and run installation.

7 *:SOA_ORACLE_HOME (default: Oracle_SOA1)
SOA Oracle Home directory (will be created under the Oracle Middleware Home MW_HOME)

8 *:IGNORE_SYS_PREREQS (default: true)
Should the Oracle installer ignore system prerequisite result?

9 *:OSB_ORACLE_HOME (default: Oracle_OSB1)
OSB Oracle Home directory (will be created relative to MW_HOME)

10 RCU:PREFIX (default: DEV)
Prefix to use for the database schemas

11 RCU:COMPONENTS (default: ["SOAINFRA", "BAM", "ORASDPM", "MDS"])
Array of schema components to be installed

12 RCU:PASSWORD
Password for your schemas. The same password will be used for all schemas

13 RCU:DB_CONNECT_STRING
Database connection string. For an Oracle database, it's host:port:SID. Please refer to RCU guide for more details.

14 RCU:DB_USER (default: SYS)
Database user that has DBA or SYSDBA privileges in order to create the RCU schemas.

15 RCU:DB_ROLE (default: SYSDBA)
Database role

16 RCU:DB_PASSWORD
Password for database user specified above

17 SOA_Suite_for_Developers_domain:INCLUDE_OSB (default: true)
Include OSB for Developers component in this domain? (true/false)

18 SOA_Suite_for_Developers_domain:INCLUDE_BPM (default: true)
Include BPM Suite for Developers component in this domain? (true/false)

19 SOA_Suite_for_Developers_domain:ASERVER_PORT (default: 7001)
Listen port for AdminServer

20 SOA_Suite_for_Developers_domain:ASERVER_SSL_PORT
SSL listen port for AdminServer (leave blank to disable SSL)

21 SOA_Suite_for_Developers_domain:DOMAIN_NAME (default: soa_domain)
Name of domain

22 SOA_Suite_for_Developers_domain:DOMAIN_PASSWORD
Password for domain administrator user (weblogic)

23 SOA_Suite_for_Developers_domain:DOMAIN_DIR (default: /oracle/middleware/user_projects/domains)
Domain directory under which domain should be created

	
###Blueprint Canvas diagram for your reference: 

###Ready to go for deployment

###Smoke test after deployment:

After deployment is successful, you may start using the application(s) immediately. Open a browser window and visit the consoles of the various products that were enabled to be installed. Following are the URLs for a standard default installation of the product(s). Please replace "hostname_or_ip" with the actual hostname or IP address that was provisioned by the cloud provider. Login as the user weblogic with the password specified during deployment.

* WebLogic admin console
http://hostname_or_ip:7001/console

* SOA Suite and EM console
http://hostname_or_ip:7001/em

* BPM composer
http://hostname_or_ip:7001/bpm/composer

* OSB console
http://hostname_or_ip:7001/sbconsole

