Update: November 7, 2017

## 0.1 Introduction

This lab is part of the APAC Cloud Test Drive and is the 2nd lab about creating microservices

## 0.2 Objectives

- Import Code from external Git Repository
- Build and Deploy project using Developer Cloud Service and Oracle Application Container Cloud Services

## 0.3 Required Artifacts

- The following lab requires an Oracle Public Cloud account that will either be applied by yourself or supplied by your instructor.
- IDE environment and GIT client in your local computer in the **previous lab**. The instructions assume you are using Brackets Editor in your local host computer. **The details of installing Brackets Editor are covered in the previous lab** and can also be found [here](../Java%20Apps/brackets.md).

## 0.4 Special Notes

- Please be careful when you copy-n-paste. Additional **WHITE SPACE** *before* or *after* the information you've copied might cause error.

# 1. Create QR Code Generator Microservice

## 1.1 Create Initial Git Repository - QR Code Generator

1. Login to Developer Cloud Service if you haven't done so. If you are in the Cloud Dashboard, you can use Developer Cloud Service Hamburger Menu to navigate to DevCS.

![](images/001.dashboard.png)

2. The Developer Cloud Service landing page should show the project we've created in the previous lab. Just click the project name and navigate to the project main page.

![](images/001.landing.png)

3. **If you are already in Developer Cloud Service, you can go to project main page by clicking `Project` in the `left hand navigation panel`**  

![](images/002.createrepo.png)

   On the right side in the **REPOSITORIES** section, click on **New Repository** to create a new Git Repository.

![](images/102.newrepo.png)

4. In the New Repository wizard enter the following information and click **Create**.

  - **Name:** `QRCodeMicroservice`
  - **Description:** `Microservice to generate Offer QR Code. The QR Code will contains an URL of the actual Offer.`
  - **Initial content:** `Import existing repository`
  - **Enter the URL:** `https://github.com/APACTestDrive/QRCodeMicroservice.git`

```diff
-Please BE CAREFUL that you have not added extra white space before or after the information when copy-n-paste
```

![](images/103.repoclone.png)

5. You have now created a new Git repository stored within the Developer Cloud Service that is based on an existing repository

![](images/104.repocreated.png)

## 2.2 Modify the sample program code to reflect your own environment

### 2.2.1 Clone Project to Bracket Text Editor

This Lab assumes your have direct connection to public Internet, i.e. **NOT behind proxy**

1. Start Brackets Text Editor, by double click the **Brackets** desktop icon, [Start] Menu button, or the correspond short-cut in your computer.

![](images/110.startbrackets.png)

2. In the **File** pull-down menu, choose **Open Folder**

![](images/111.open.png)

3. Select a desired folder to store the source code in your local harddisk, e.g. **d:\oracle** in the left hand side and click **[Create Folder]** at the top right hand corner - `this will create a new folder under the folder you've selected`.

![](images/112.createfolder.png)

4. Enter **QRCodeMicroservice** as the folder name. Then Click any space (e.g. in the size column) next to the name

![](images/113.gotofolder.png)

5. Click **[ Open ]** button to open the newly created project folder.

![](images/114.opennew.png)

6. Back in **Developer Cloud Service**, in your **QRCodeMicroservice Git Repository**. Click **HTTP** to display the Git HTTP URL, click the **Copy** button to copy the URL.

![](images/115.copyurl.png)

7. Back in the Bracket editor, click on **GIT** icon on the right hand side of the editor.

![](images/116.gitbutton.png)

8. In the Git panel, click **[ Clone ]**

![](images/117.gitclone.png)

9. Paste the GIT URL that you copied from Developer Cloud Service. Username should be populated automatically. Enter the password and select **Save credentials to remote url**

10. Click **[OK]** button

![](images/118.gitlogin.png)

11. Wait for Brackets to clone your remote project to local folder.

![](images/119.gitwaitclone.png)

12. You now have a local copy of the Git Repository.

![](images/120.cloned.png)

### 2.2.2 Edit the source code to fit your environment

1. Open the server.js file (double click) in Brackets

![](images/121.openjs.png)

2. In line 12, change the URL to your identity domain, i.e. in the format of **`http://<IP Address used in #1 JavaApp Lab>/ptmgt/v1/offer/`**. As you can see, this is the URL of the **Offer REST API Microservice**

![](images/122.line12.png)

3. Save the file. (**Ctrl-S** or choose from pull-down menu **File > Save**)

![](images/123.save.png)

### 2.2.3 Create a new Branch and Commit

1. In the left hand navigation panel, select **master** and click **Create new branch...**

![](images/124.branch.png)

2. In the pop-up window, enter `ChangeURL` for branch name and click **Ok**

![](images/125.changeurl.png)

3. Check the box next to **Commit** to select all modified files - this means the checkbox below (server.js) will automatically be checked.

![](images/126.commitcheck.png)

4. Click **Commit**

![](images/127.commit.png)

5. In the pop-up enter the **comment** `modify source code to use correct URL` and click **OK**. This will commit the changes to your LOCAL GIT REPOSITORY. (You can ignore the code inspection problems. You can review the code changes before confirmation)

![](images/128.commitmsg.png)

6. Click **Git Push** icon.

![](images/129.push.png)

7. In the pop-up window, leave all defaults and click **Ok**.

![](images/130.pushok.png)

8. Once Git Push completes, click **Ok**

![](images/131.pushdone.png)

9. You have push the changes to Developer Cloud Service. If you like, you can go to **Developer Cloud Service** to check the pushed branch. You will something like this.

![](images/132.newbranch.png)

### 2.2.4 Create Merge Request in Developer Cloud Service to uptake the code

1. In Developer Cloud Service, click on **Code** tab. If you are not viewing the QRCodeMicroservice repo, change to the QRCode Repo.  

![](images/141.checkbranch.png)

2. Select ChangeURL branch

![](images/142.changeurlbranch.png)

3. Once you are in the ChangeURL branch. You should be able to view the recent commit that we made to branch from Brackets.

![](images/143.changes.png)

4. Now, a merge request can be created to merge the code - click on **Merge Requests** to go the merge request panel.

![](images/144.mergereq.png)

5. and then click on the **New Merge Request** button.

![](images/145.newmerge.png)

6. Enter the following information into the new merge request and click **Next**

  - **Repository:** `QRCodeMicroservice.git`
  - **Target Branch:** `master`
  -	**Review Branch:** `ChangeURL`

![](images/146.createreq.png)

7. Enter for following information into **Details** and click **Next**

  - **Summary:** `Merge Request for branch ChangeURL`
  - **Reviewers:** `Choose the user you are working on` (e.g. Cloud Admin, John Dunbar, etc)

![](images/147.req2.png)

8. Review the request and click **[+ Create]** button.

![](images/148.reqcreate.png)

9. Now, the merge request has been created. We will approve the request in the next section.

### 2.2.5 Merge the Branch

1. click on the **Merge Request**. Select the request we just created and we can review the request.

![](images/151.requestdetails.png)

2. Once the request has loaded, select **Change Files** tab. Review the changes. You can add your comment before approve the request.

![](images/152.changedfiles.png)

3. if you like you can click the **[Approve]** button to add comments

![](images/153.approve.png)

4. Enter some comments, e.g. `approved` and click **OK**.

![](images/154.approvmsg.png)

5. You can see the request is now approved by reviewer. Click **Merge** button to proceed merging

![](images/155.clickmerge.png)

6. leave the defaults OR enter your desired comment. If you check **Delete branch**, the ChangeURL branch will be deleted after the merging. Click on **Create a Merge Commit** button.

![](images/156.commitmerge.png)

7. Now the code merge had been committed and we can build the microservice. 	

![](images/157.merged.png)

## 2.3 Create Default Build and Deployment Process - QR Code Generator

Now that we have the source code in our Developer Cloud Service managed Git Repository, we need to create a build process that will be triggered whenever a commit is made to the master branch. We will setup a **shell script** build process in this section.

### 2.3.1 Create Default Build Process - QR Code Generator

1. Click **Build** on the navigation panel to access the build page

![](images/161.navibuild.png)

2. Click **[+ New Job]**

![](images/162.createnewbuild.png)

3. In the New Job popup window, enter `QR Code Generator Build` for Job Name and click **Save**.

```diff
-Please BE CAREFUL that you have not added extra white space before or after the information when copy-n-paste
```

![](images/163.newjob.png)

4. You are now placed into the job configuration screen.

![](images/164.buildscreen.png)

5. Click the **Source Control** tab. Select **Git** radio button. In the Repositories section, select **QRCodeMicroservice.git** from the URL drop down.

	**Note:** Make sure you select the Git repository for the QR Code Microservice.

![](images/165.srcctrl.png)

6. Click **Triggers** tab. Check **Based on SCM polling schedule**.

![](images/166.trigger.png)

7. Click the **Build Steps** tab, click **Add Build Step** and select **Execute shell**.

![](images/167.stage.png)

8. In the Command textarea, enter: `npm install`

![](images/168.npm.png)

9. Click the **Post Build** tab. Check **Archive the artifacts**. For File to Archive, enter `**/target/*` and verify **GZIP** is chosen as the Compression Type.

![](images/169.pb1.png)

10. Click **Save** to complete the configuration.

![](images/170.pbsave.png)

11. A build should start automatically within 1-2 minutes. If it does not start automatically, click on the **[ Build Now ]** button.

![](images/171.now.png)

12. The status will change to something similar to the following diagram.

![](images/172.queue.png)

Building stage: please wait - it might takes a few minutes before the job change form queued to running

![](images/173.building.png)

13. The build will take serval minutes to complete. Wait for the build to complete before continue to the next step - **as we need the build artifact to create the deployment configuration**.

![](images/174.buildsuccess.png)

### 2.3.2 Create Default Deployment Process - QR Code Generator

1. Click **Deploy** to access the Deployments page

![](images/181.navideploy.png)

2. Click the **[+ New Configuration]** button.

![](images/182.newdeploy.png)

3. Enter the following data:

  - **Configuration Name:** QRCodeGeneratorDeploy
  - **Application Name:** qrcodegenerator
  
```diff
-Please BE CAREFUL that you have not added extra white space before or after the information when copy-n-paste
```

![](images/183.createdeploy.png)

4. Next to the right hand side of **Deployment Target**, click the **[New]** button and select **Application Container Cloud...**

![](images/020.deployaccs-reuse.png)

5. A window **Deploy to Application Container Cloud** will popup, confirm the information and **ENTER the password**, then click **[Test Connection]** button.   

  - **Data Center:** `your datacenter, e.g. em2, em3, etc`
  - **Identity Domain:** `your  Identity Service Id, which can be obtained from:`  
    Access to Application Container Cloud Service dashboard  
    ![](images/185.test.accs.png)
    Copy the `Identity Service Id` from the ACCS dashboard, and paste the Id into **Identity Domain** text box  
    ![](images/185.test.accs1.png)
  - **Username:** `username to login to MyService, e.g. cloud.admin, etc`
  - **Password:** `password of the cloud user`

![](images/185.test.png)

6. Once test is success, click **Use Connection**

![](images/186.testgood.png)

7. In the ACCS Properties, set

  - **Runtime** to `Node`
  - **Subscription** to `Hourly`
  - Set **Type** to `Automatic` and **CHECK** `Deploy stable build only`

**MAKE sure you select Node as the Runtime**

![](images/187.choosenode.png)

8. Select from the **Job**, this name should match the build job above, e.g. `QR Code Generator Build`. Select from the **Artifact**, this name should match the archive artifact above and the package.json of your source code, e.g. `target/qrcodegenerator.zip`  

![](images/188.choosejob.png)

9. Check `Include ACCS Deployment` box and enter the following json

```json
{
	"memory":"1G",
	"instances":"1"
}
```

![](images/024.json.11.png)

10. After fill in the above information, click **Save** button.

![](images/189.depsave.png)

11. In your deployment job, click the gear drop down and select **Start**

![](images/190.start.png)

12. The deployment job will be put into a queue for process. Wait until the message **Starting application** changes to **Last deployment succeeded**. Ask for help from your instructor if the deployment fails.

![](images/191.deployed.png)

## 2.4 Login to Oracle Application Container Cloud Service

1. Navigate back to the Oracle Public Cloud tab. Click **Dashboard** to return back to main Cloud Service Dashboard.

2. On the Application Container Cloud Service (ACCS) click the humburger button and select **Open Service Console**

![](images/192.accs.png)

3. On the ACCS Service Console you can view all the deployed applications including our newly create **qrcodegenerator**.

![](images/193.accsqr.png)

4. Copy the URL and paste it into the address bar of a new tab to bring up the application.

  Be reminded that you will need the REST endpoint and the **offer id** in order to generate a QR code.

  The final URL should looks like this

	{URL copied from ACCS Service Console}/ctdqr/v1/offer/10001  
	or  
	https://qrcodegenerator-{your-identity-domain}.{datacenter-location}.oraclecloud.com/ctdqr/v1/offer/10001

![](images/194.qrurl.png)		

5. the QR Code in the browser will look like this

![](images/195.codepic.png)

```diff
+ you might want to copy your OWN URLs for QR Code API
+   {URL copied from ACCS Service Console}/ctdqr/v1/offer/
+   {URL copied from ACCS Service Console}
+ and put it in, e.g. Notepad
+   You will need to use it later, e.g. Lab 304 Step 27.
```

**OPTIONAL STEP:** if you use a QR Code reader (e.g. Mobile App), you can decode the QR Code

![](images/196.reader.png)

# Congratulation! You've completed the Microservice Lab.

[go back to the Cloud Test Drive Main Page](../README.md)
