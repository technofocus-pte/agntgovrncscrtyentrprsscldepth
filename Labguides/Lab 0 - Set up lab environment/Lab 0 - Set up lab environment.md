<!--
lab:
  title: Lab 0 Set up lab environment
  description: In this lab, you will acquire Power Apps trial license.
You will also add users and assign licenses to them at the same time.
  duration: 10 minutes
  level: 100
  islab: true
-->

# Lab 0: Set up lab environment

**Estimated Duration:** 10 min

### Objective

In this lab, you will acquire Power Apps trial license. You will also add users and assign licenses to them at the same time.

### Task 1: Assign Power Apps trial license

1. Open a web browser on your VM and go to +++https://powerapps.microsoft.com/en-us/free/+++.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%200%20-%20Set%20up%20lab%20environment/media/image1.png)

1. Select **Start free**.

    ![A person with his arms crossed Description automatically generated](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%200%20-%20Set%20up%20lab%20environment/media/image2.png)

1. Enter your **Office 365 admin credential**, check the checkbox to **accept the agreement** and click on **Start your free trial**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%200%20-%20Set%20up%20lab%20environment/media/image3.png)

1. Enter **password of your Office 365 tenant id** and then select **Sign in**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%200%20-%20Set%20up%20lab%20environment/media/image4.png)

1. Select **Yes** on **Stay signed in?** pop-up window.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%200%20-%20Set%20up%20lab%20environment/media/image5.png)

1. You can now see **Home page of Power Apps.** From the environment selector, select the developer environment – **Dev One** which is created for you.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%200%20-%20Set%20up%20lab%20environment/media/image6.png)

1. Open the new tab and go to Power Platform admin center by navigating to +++https://admin.powerplatform.microsoft.com+++ and if required, sign in using your given Office 365 admin tenant credentials. Close the pop-up that says, ‘Welcome to the new Power Platform admin center’.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%200%20-%20Set%20up%20lab%20environment/media/image7.png)

1. From the left navigation pane, select **Manage** \> **Environments** and then you can see, **Dev One** is your Dataverse environment.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%200%20-%20Set%20up%20lab%20environment/media/image8.png)


### Task 2: Create Microsoft 365 Users

1. Open **Import_Users_Contoso.csv** file from **C:\Labfiles** folder on your Lab VM.

1. Under the **Username** column, update the tenant name to reflect your Office 365 tenant name for each user in the list and then save as a CSV format file.

    >[!Note] Your Office 365 tenant is @lab.CloudCredential(M365).AdministrativeUsername,
    > your domain would be @lab.CloudCredential(M365).TenantPrefix.
  
1. Navigate to the Microsoft 365 admin center using +++https://admin.microsoft.com+++

1. From the left navigation, select **Users** \> **Active users** page, click **Add multiple users**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%200%20-%20Set%20up%20lab%20environment/media/image9.png)

1. On the Upload a CSV file with user info pane, select **I’d like to upload a CSV with user information** and then click **Browse**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%200%20-%20Set%20up%20lab%20environment/media/image10.png)

1. In the Open dialog box, navigate **C:\Labfiles\\ Import_Users_Contoso.csv** and click **Open**.

    ![A screenshot of a computer Description automatically generated](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%200%20-%20Set%20up%20lab%20environment/media/image11.png)

1. Once the CSV file passed verification, click **Next**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%200%20-%20Set%20up%20lab%20environment/media/image12.png)

    >[!Note] If you receive an error message, review your CSV file for errors, and fix them

1. On the Licenses pane, select all the license check boxes and click **Next**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%200%20-%20Set%20up%20lab%20environment/media/image13.png)

1. On the **Review and finish adding multiple users** pane, click **Add users**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%200%20-%20Set%20up%20lab%20environment/media/image14.png)

1. On the **You added 11 users** pane, click **Close**.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%200%20-%20Set%20up%20lab%20environment/media/image15.png)

1. On the **Active users** page, select all the new users, (except MOD Admin) then click on **Reset password**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%200%20-%20Set%20up%20lab%20environment/media/image16.png)

1. To reset the same password for all the users, uncheck all check boxes and enter password as : +++Pa$$w0rd@124+++ and then click on **Reset password**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%200%20-%20Set%20up%20lab%20environment/media/image17.png)

1. On the **Reset password** pane, click **Close**.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%200%20-%20Set%20up%20lab%20environment/media/image18.png)

    > **Summary:** In this lab, you acquired Power Apps trial license and
    > also added users from the Microsoft 365 admin center.
