# ORACLE Cloud Test Drive #
-----
## Installation and Usage of Oracle VM VirtualBox for Cloud Test Drive ##

VirtualBox is a cross-platform virtualization application. What does that mean? For one thing, it installs on your existing Intel or AMD-based computers, whether they are running Windows, Mac, Linux or Solaris operating systems. Secondly, it extends the capabilities of your existing computer so that it can run multiple operating systems (inside multiple virtual machines) at the same time. So, for example, you can run Windows and Linux on your Mac, run Windows Server 2008 on your Linux server, run Linux on your Windows PC, and so on, all alongside your existing applications. You can install and run as many virtual machines as you like -- the only practical limits are disk space and memory.  
VirtualBox is deceptively simple yet also very powerful. It can run everywhere from small embedded systems or desktop class machines all the way up to datacenter deployments and even Cloud environments.  
The following screenshot shows you how VirtualBox, installed on a Mac computer, is running Windows 8 in a virtual machine window:

![](images/virtualbox/vm-vista-running.png)

### Prerequisites ###
This lab guide assumes the following:
- Internet access available (to download installer and extension pack, check or copy files from instructor)
- Use Microsoft Windows as host operating system https://www.virtualbox.org/manual/ch01.html#hostossupport
- A copy of *Open Virtualization Format (.ova)* VM file

#### Installation of Oracle VM VirtualBox ####

1. Go to [VirtualBox Welcome Page](https://www.virtualbox.org/) and click `Download VirtualBox X.X` button at the middle.

![](images/virtualbox/00.virtualbox.download.png)

2. From the download page, select your operating system installer download link under *VirtualBox X.X.XX platform packages*.  
   This guideline uses `Windows hosts` as example.

![](images/virtualbox/01.virtualbox.download1.png)

3. On pop-up, click `Save File` and `OK` to save the VirtualBox installer to your destinated location.

![](images/virtualbox/02.virtualbox.save.png)

4. Launch the VirtualBox installer executable from your saved destination.

![](images/virtualbox/03.virtualbox.installer.png)

5. Click `Next` on installer launched.

![](images/virtualbox/04.virtualbox.installer1.png)

6. On **Custom Setup** page, browser and select VirtualBox destination folder for installation, then click `Next`.

![](images/virtualbox/05.virtualbox.installer2.png)

7. Check the required options and click `Next`.

![](images/virtualbox/06.virtualbox.installer3.png)

8. On `Warning: Network Interfaces` page, click `Next`.

![](images/virtualbox/07.virtualbox.installer4.png)

9. Click `Install` to proceed installation process.

![](images/virtualbox/08.virtualbox.installer5.png)

10. Wait a couple of minutes for the installation complete.

![](images/virtualbox/09.virtualbox.installer6.png)

11. Check the `Start Oracle VM VirtualBox X.X.XX after installation` option and then click `Finish`.

![](images/virtualbox/10.virtualbox.installer7.png)

12. The **Oracle VM VirtualBox Manager** window start.

![](images/virtualbox/11.virtualbox.start.png)

#### Usage of Oracle VM VirtualBox ####

13. Click `File` from top menu bar, and then select `Import Appliance...`.

![](images/virtualbox/12.virtualbox.file.png)

14. Click the folder icon. 

![](images/virtualbox/12.virtualbox.import.png)

15. Browser and select the *Open Virtualization Format (.ova)* VM file which was provided by instructor.

![](images/virtualbox/13.virtualbox.import1.png)

16. On Appliance settings, keep the default values, then click `Import`.

![](images/virtualbox/14.virtualbox.import2.png)

17. Wait a couple of minutes for the VirtualBox Manager to import .ova file into VM locally.

![](images/virtualbox/15.virtualbox.import3.png)

18. On completion of VM import, a new entry named **DevOpsWorkshopV3.04** is shown on the VM list in VirtualBox Manager.

![](images/virtualbox/16.virtualbox.import4.png)

19. Back to [VirtualBox Download Page](https://www.virtualbox.org/wiki/Downloads), click `All supported platforms` link next to **VirtualBox X.X.XX Oracle VM VirtualBox Extension Pack.

![](images/virtualbox/17.virtualbox.extension.png)

20. Save the Oracle VM VirtualBox extension pack to your destinated location.

![](images/virtualbox/18.virtualbox.extension1.png)

21. Double click or launch the extension pack.

![](images/virtualbox/19.virtualbox.extension2.png)

22. This will bring up the VM VirtualBox Manager with extension pack installation dialog.  
    Click `Install` button in the pop-up window.

![](images/virtualbox/20.virtualbox.extension3.png)

23. Scroll to the end of *VirtualBox License* and click `I Agree` button at bottom of winodw. (read optionally)

![](images/virtualbox/21.virtualbox.extension4.png)

24. **Oracle VM VirtualBox Extension Pack** installation is done, click `OK`.

![](images/virtualbox/22.virtualbox.extension5.png)

25. Now, everything required for running VM is ready, select the new VM **DevOpsWorkshopV3.04** and click `Start` button.

![](images/virtualbox/23.virtualbox.extension6.png)

26. A new window hosting the VM content is shown upon VM started.  
    Keep the default option: **Oracle Linux Server 7.2, with Unbreakable Enterprise Kernel 3.8.13-118.9->**

![](images/virtualbox/24.virtualbox.vm-start.png)

27. Wait a couple of minutes for the Oracle Linux inside the VM startup, finally, the Linux desktop shall be shown.  
    You will use the **Eclipse** and *brackets* desktop icons in lab exercises today.

![](images/virtualbox/25.virtualbox.vm-started.png)

28. You have finished installation and usage of Oracle VM VirtualBox.

[Back to JavaAppLab Home](README.md)
