[wl]: https://raw.github.com/vmware-applicationdirector/solutions-import-beta/AD-ADFS-Blueprint/AD-ADFS-Blueprint.png
[w2]: https://raw.github.com/vmware-applicationdirector/solutions-import-beta/AD-ADFS-Blueprint/AD-ADFS-Blueprint_ActiveDirectory.png
[w3]: https://raw.github.com/vmware-applicationdirector/solutions-import-beta/AD-ADFS-Blueprint/AD-ADFS-Blueprint-ADFS.png
[w4]: https://raw.github.com/vmware-applicationdirector/solutions-import-beta/AD-ADFS-Blueprint/AD-ADFS-Blueprint-Deploy.png
[w5]: https://raw.github.com/vmware-applicationdirector/solutions-import-beta/AD-ADFS-Blueprint/AD-ADFS-Blueprint-ExecutionPlan.png
[w6]: https://raw.github.com/vmware-applicationdirector/solutions-import-beta/AD-ADFS-Blueprint/ActiveDirectoryUsersandComputers.png
[w7]: https://raw.github.com/vmware-applicationdirector/solutions-import-beta/AD-ADFS-Blueprint/AD-ADFS-Console.png

## Success
Your application has been successfully imported and ready to go but first there are a few final steps you need to follow before you can perform a deployment.

#### Prerequisites:  
Install and configure VMware vFabric Application Director 5.0 with vCloud Director. See the product documentation for information about installing and configuring Application Director.  

1.Get the ADFS 2.0 installer and copy it to downloadable location
http://www.microsoft.com/en-in/download/details.aspx?id=10909&hash=VrATgGfA8ZnXqoooj1Xqtr0uVhlPvHeSKKlmgVKbg7rsytvNjndrF%2fzelBesONw7N6%2fiUvPD9Ps0k3ds6sR8jw%3d%3d  

2.Get User Certificates in .pfx and .p7b format and copy it to downloadable location
Please note that user certificate name should match with DNS name of adfs host. e.g. If you have specified ADFS host name as ADFSHost and DNS name as testad.com, then certificate name should be ADFSHost.testad.com  

Steps to export in *.pfx format:  
- Open Server Manager, Click on Roles.  
- On IIS Manager, click Server Certificates  
- Select the certificate and click on export  
- Browse and select location to export and type for export as *.pfx. Enter password and click ok  
- User needs to enter the location and the password for the same in the export dialog  
- Certificate gets exported  

Steps to export in *.p7b format:  
- Open Management Console. Go to Start, type MMC and enter  
- Click File->Add/Remove Snap-in  
- Select Certificates and click Add  
- Select Computer Account and click next  
- Click Finish. Click Ok on Add/Remove Snap-in dialog  
- Now go to Personal Certificates, select the certificate to be exported, right click -> All tasks -> Export  
- On Certificate export wizard click next  
- On Export Private Key step, select No, do not export private key, select next  
- Select .P7B format and select checkbox 'Include all certificates in the certification path if possible' click next  
- Enter path and filename and click next  
- Click Finish and certificate gets exported  

3.Create the vApp Template with OS Windows 2008 R2 Enterprise having application director agent.  See application director documentation for how to create vApp Template for windows.
 
#### Set Up:
Click on the "Try" link of this solution to import the blueprint.  Update the Application Director URL and password. Click on Import File button. It will import the blueprint in your application director. Once blueprint is imported, it will show you the page which explains the steps to be done after import.

Following are the steps to be done after import:  
1.Create the vApp Template with OS Windows 2008 R2 Enterprise having application director agent and map it to logical template 'W2K8 R2 Ent SP1 For AD' that is used in blueprint.   

2.Once blueprint is imported, login to Application Director and check application with name 'AD and ADFS'. Click on Application name and go to blueprint. It will show following:

[![AD-ADFS-Properties][wl]][wl]

Following properties to be updated in blueprint or in deployment profile:  
**For ActiveDirectory Service:**  
- netbios and dnsname: Netbios name will be part of DNS name e.g. if DNS name is adtest.com then netbios name should be adtest  
- password: Password that should be set for local admin  
- safepass: Safe mode recovery password, it should be complex password having at least on1 uppercase letter, one lowercase letter, number and special characters

[![AD-ADFS-Properties][w2]][w2]

**For ADFS service:**  
- adfsinstalller: Downloadable path of ADFS 2.0 installer from where application can download the installer  
- local_admin_pass: Local admin password of ADFS machine  
- usercertpb: Downloadable path of User Certificate in .p7b format  
- usercert: Downloadable path of User Certificate in .pfx format  
- usercert_password: Password of user certificate

[![AD-ADFS-Properties][w3]][w3]

#### Deployment:  
1.Now click on deploy to deploy the application.   
2.Enter name for deployment profile  
3.Step1: Deployment Environment tab will be displayed. Enter proper values as per your environment and click next  
4.Step2: Application Properties  
- Node tab: Enter/Update proper values for nodes i.e. CPU, Memory, Hostname  
- Service tab: As mentioned above property values for each service can be updated directly in blueprint or in deployment profile. Enter/Update property values for each service i.e. Active Directory and ADFS_Service service.

[![AD-ADFS-Properties][w4]][w4]  

5.Step3: Execution plan: It will show following screenshot

[![AD-ADFS-Properties][w5]][w5]  

6.Step 4: Review: Click Deploy
  It'll start the deployment. Wait till deployment completes.

#### Deployment Verification:  
Once deployment is complete, you can use following steps to verify the deployment:  

**For AD Setup:**  
1.Login to the AD machine with Active Directory domain credentials which were used while deployment  
2.Click on Start > Administrative Tools. Following entities associated the AD setup will be displayed:
-	Active Directory Administrative Center  
-	Active Directory Sites and Services  
-	Active Directory Users and Computers  
-	Active Directory Domains and Trusts

Click on Active Directory Users and Computers > Computers. It will display the computers in the AD domain.

[![AD-ADFS-Properties][w6]][w6]  

3.You can also check Server Manager to verify that the machine is added to domain that is created. Click on Start > Administrative Tools. Open the Server Manager. It shows that machine is added to domain.

**For ADFS Setup:**  
1.Login to the ADFS machine with AD domain credentials  
2.AD FS 2.0 Management menu is displayed when Start > Administrative Tools is clicked  
3.Click on ADFS 2.0 Management to view the console. Following screen will be displayed screen if ADFS is successfully deployed: 

[![AD-ADFS-Properties][w7]][w7]  
