# ORACLE Cloud Test Drive #
-----
## 101: Create Oracle Developer Cloud Service Loyalty Management application project using initial GitHub repository ##

### Introduction ###
This tutorial demonstrates how to:
- Create Oracle Developer Cloud Service project using existing external Git repository - GitHub

### About the Exercise Today ###
In this exercise, we will:
- Create a new Developer Cloud Service Project for the Loyalty Management System
- Create a new Developer Cloud Service Git Repository to store the Loyalty Management Java Application Source Code
- Clone an external Git repository, which is stored in Github, to the Developer Cloud Service Git Repository create above

### Prerequisites ###
- Oracle Public Cloud Service account including Developer Cloud Service (Check with instructor if you don't have one)

----

#### Sign In to Oracle Cloud ####

1. Open a browser and go to [cloud.oracle.com](https://cloud.oracle.com). Click **Sign In**.
![cloud.oracle.com](images/sign-in/sign.01.cloud.oracle.com.png)

2. Follow the lab access document provided by instructor, per each of Lab section, you should be able to locate corresponding datacenter info, for example:  
![](images/sign-in/sign.01.cloud.account.png)  
or  
![](images/sign-in/sign.01.cloud.account1.png)  

Because this is the first Lab 1xx - Java App, we need to login to DevCS and therefore:  
Select `Traditional Cloud Account`, then select    
    `US Commercial 2 (us2)`   
or    
    `EMEA Commercial 2 (em2)`    
according to the datacenter of your environment listed in access document.  Click **My Services** button.
![](images/sign-in/sign.02.select.datacenter.png)

3. Enter the **Developer Cloud Service \(DevCS\)** identity domain and click **Go**. The identity domain and associated credential should be provided by instructor.
![](images/sign-in/sign.03.identity.domain.png)

4. Enter the DevCS username and password of user with Service Administrator role. Click **Sign In**.
![](images/sign-in/sign.04.credentials.png)

5. After a successful login you will see your Dashboard.  
On the Dashboard there are predefined tiles for different services. If the **Developer Cloud Service** tile doesn't appear, click **Customize Dashboard** and mark the **developer** service to show on the dashboard.
![](images/sign-in/sign.05.dashboard.new.png)
![](images/sign-in/sign.06.customize.png)

#### Create Oracle Developer Cloud Service project ####

6. Now, find the Developer Service tile and click the hamburger icon. In the dropdown menu click **Open Service Console**.

![](images/101/01.dashboard.new.png)

7. Log in to Oracle Developer Cloud Service and create a new project.

![alt text](images/101/02.new.project.png)

8. Enter the name of the project and set the desired properties.   
	**Name:** `APAC Cloud Test Drive XX` (XX - Use your assigned ID, e.g. 01)  
	**Description:** `APAC Cloud Test Drive project hub XX` (XX - Use your assigned ID, e.g. 01)  
	and click **Next**

![](images/101/02.new.project.detail.png)

9. Select *Empty Project* as template and click **Next**

![](images/101/03.emptyproject.png)

10. Choose `MARKDOWN` as Wiki Markup and click **Finish**

![](images/101/04.finish.png)

11. **Wait** for the Developer Cloud Service Project got provisioned.

![](images/101/05.wait.png)

12. You will see the project main screen once the project is ready. In the right hand pane, make sure you are in the `Repositories` tab. Click the [ **+ New Repository** ] button to create a new Git repository.

![](images/101/06.newrepo.png)

13. Enter the following information for the New Repository   
   Name: `LoyaltyManagement`   
	 Initial content: select `Import existing repository`   
   Enter or copy the `https://github.com/APACTestDrive/LoyaltyManagement.git` as the repository address.   
Click the [ **Create** ] button

![](images/101/07.repoinfo.png)

14. You have now created a new Git repository with source code stored within the Developer Cloud Service that is based on an existing repository.

![](images/101/08.repocreated.png)


You have finished this lab section.

[Procced to Next - 102: Define Continuous Integration 'Build' and 'Deploy' Configuration in Oracle Developer Cloud Service](102-JavaAppsLab.md)

or

[Back to JavaAppsLab Home](README.md)
