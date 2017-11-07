
# ORACLE Cloud Test Drive #

## Introduction ##
We have huge reliance on mobile services for our daily life. Due to this trend, enterprises are eager to build more and more mobile applications for better customer experiences, operational excellences and higher business values in their businesses. Therefore, we can say that Mobile is the key of Digital Transformation. And mobile application development in businesses is much more of a reality – Let's see what challenges of mobile application development in terms of business and technical view are.

### Technical Challenges in Mobile ###
As well as Business Challenges, enterprises have some of difficulties in developing mobile applications. To develop mobile applications, we need to have the expertise in:
+ Developing to and supporting multiple platforms (Android, iOS, Windows, etc.)
+ Prepare environments for dev, test and production
+ How to monitor and analyze mobile services
+ Security and identity protocols and policies to different backends
+ Integration with a variety of backends
+ What tools do you use to build them?
![](../common/images/mobile/Technical_Challenges_in_Mobile.PNG)

## Oracle Mobile Solution Strategy ##
To overcome the above challenges, Oracle encourages developers to use any of the popular tools available – whether it’s native development with iOS and Android, to 3rd party and open frameworks like Ionic, Angular, Sencha, and Xamarin. We call it "Mobile Client Agnostic". Oracle also incorporate mobile services that offer data sync, storage, location services, messaging, access to local services like camera, contacts, GPS, etc. There’s a trend towards low code, no code development - Oracle supports this trendy tool called MAX (Mobile Application Accelerator) as part of Mobile Cloud Service (MCS).
![](../common/images/mobile/Oracle_Mobile_Solution_Strategy.PNG)

In summary, Oracle provides end to end solution to give you overcoming notable business and technical challenges.

### Oracle Mobile Services ###
Here you can see which mobile services are ready for you through just accessing Oracle MCS (Mobile Cloud Service) as below:
+ Out of the box mobile services (Platform APIs): We are providing prebuilt, tested and optimized mobile services like analytics, push notification, offline data synchronization, location, object storage, database, app polices, API management, integration management, security and user management, and more features like intelligent bot are coming.
+ In addition to the Platform APIs, you can develop custom APIs and code to extend your mobile services. (e.g.: SNS integration, Google Map integration, external system integration, etc.) In other words, mobile applications can call custom APIs as wells as platform APIs to interact various data sources.
+ For client IDEs to develop mobile applications, we can support any IDE as well as mobile frameworks like Oracle MAX (Low code development), JET (JavaScript-based Hybrid App Dev.) and MAF (Java-based Hybrid App Dev.)

![](../common/images/mobile/Oracle_Mobile_Services.PNG)

If you want to know about more details on the above mobile services, please refer to [the following link](https://docs.oracle.com/en/cloud/paas/mobile-cloud/index.html).

### About the Exercise Today ###
The hard part of mobile development is integration and managing all server-side services. In this exercise, you will see how easily you can enable/develop mobile services like push notification, API creation and integrations with external services to implement a mobile application called "Cafe Supremo" for loyalty management using Oracle MCS (Mobile Cloud Service).

For the loyalty management mobile application, you can make it all work and play nicely together using platform APIs (out of box mobile services) and custom APIs for external integrations by doing the below jobs through this lab.
- Import MBE (Mobile BackEnd) package and configure connectors to integrate external services, including the microservice on ACCS to generate QR code, and the service on ICS to accept or reject offer and update the existing CRM.
- Verify the endpoints and the implementation of the custom API. The custom API is imported in the MBE package, and leverage the connectors to interact with the external services.
- Set up Push Notification, and configure the Cafe Supremo mobile app to work with the MBE imported.
- Track customer behaviors like "Offer Accept by users" using custom analytics report. **[Note]** this section is optional. You can skip this section first, and come back after you complete all the other sections.

![](../common/images/mobile/CTD_About_Lab_Mobile.PNG)


### Prerequisites ###
- Bring your Android phone.
- Make sure you receive the MBE package file "package-LoyaltyMgmt_MBE0X.zip" from the instructor. "0X" in the file name should matches the postfix assigned to you in the access document. If you don't have the MBE package file or the file name doesn't match the postfix assigned to you, please contact the instructor to get the right file.
- In the end of this lab, you will configure your mobile application to work with the MBE created by yourself. You will collect all the settings in a file "Mobile_App_Settings_Sample.json". You can download an example of this file by right clicking on [this link](../common/assets/mobile/Mobile_App_Settings_Sample.json) and select "Save link as...". Once you collect all the settings in this file, you will create a QR code to represent the settings by using the [online QR code generator](http://www.qr-code-generator.com/).
- Install "Cafe Supremo" mobile application on you Android phone. If you have QR code scanner installed on your phone, install the mobile application by scanning the following QR code from your phone.

   ![](../common/images/mobile/400-Install_App_QRcode.png)

Otherwise, download the app file by right clicking on [this link](../common/assets/mobile/Cafe_Supremo.apk?raw=true). Select "Save link as..." to download it. Follow below instructions to install the mobile application.

1. Connect your device to your computer and copy an Android APK file called “Cafe_Supremo.apk” to SD card or internal storage of your device.

   ![](../common/images/mobile/401-Install_App_1.png)

2. Enable Unknown Sources in your Android device: Go to "Settings" >>" Security ">> Check the box "Unknown sources". (FYI, the menu will be slightly different by Android versions.)

   ![](../common/images/mobile/401-Install_App_2.png)

3. Open a file manager on your Android device. 

   ![](../common/images/mobile/401-Install_App_3.png)

4. Go to the same location where you put the “Cafe_Supremo.apk” file and Click the file to install. The below image shows Android APK files in case you put them in the folder called “Download”.

   ![](../common/images/mobile/401-Install_App_4.png)

5. Press “Install” button.

   ![](../common/images/mobile/401-Install_App_5.png)

6. Allow all permissions the “Café Supremo” mobile application requires by clicking “CONFIRM” button. Now you have finished the installation of the mobile application.

   ![](../common/images/mobile/401-Install_App_6.png)


---
# Lab Exercise: #
Let's explore the Mobile Service and Application Lab. Please click the below link to start your lab.

## 401: Import MBE package and configure connectors for external services ##

[Click Here.](401-MobileLab.md)

## 402: Verify and test custom APIs and implementation ##

[Click Here.](402-MobileLab.md)

## 403: Set up Push Notification and configure the mobile app ##

[Click Here.](403-MobileLab.md)

## 404: Track customer behaviors [Optional] ##

[Click Here.](404-MobileLab.md)

or

[Back to Cloud Test Drive Home](../README.md)
