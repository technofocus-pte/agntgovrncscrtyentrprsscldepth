<!--
lab:
  title: 'Lab 1: Create and manage environment using Power Platform Admin Center'
  description: In this lab, you will learn how to control who can create
and manage environments, enable or disable Administration mode in the
Power Platform Admin Center, create a custom security role, and assign
it to an administrative user.
  duration: 20 minutes
  level: 100
  islab: true
  primarytopics:
    - Office 365
-->

# Lab 1: Create and manage environment using Power Platform Admin Center

**Estimated Duration:** 20 min

### Objective

In this lab, you will learn how to control who can create and manage environments, enable or disable Administration mode in the Power Platform Admin Center, create a custom security role, and assign it to an administrative user.

## Exercise 1: Control environment creation in the Power Platform Admin Center

### Task 1: Setting an environment refresh Cadence

You can indicate how often you would prefer an environment to receive updates and features to certain Microsoft Power Platform services. You have two options to choose from after creating an environment.

**Service -** Canvas app authoring

**Frequent** - Get access the latest updates and newest features multiple times a month

**Moderate** - Get access to updates and features at least once a month

To set refresh cadence:

1. Browse to the Power Platform admin center at +++https://admin.powerplatform.microsoft.com+++ and sign in with your Office 365 tenant credentials.

1. From left navigation pane, select **Manage** \> **Environments** and then click on the **Dev One** environment.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%201%20-%20Create%20and%20manage%20environments/media/image1.png)

1. Click on **Edit** in details section.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%201%20-%20Create%20and%20manage%20environments/media/image2.png)

1. Under **Refresh cadence**, choose the **cadence** type - +++Frequent+++ and then click on **Save** button.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%201%20-%20Create%20and%20manage%20environments/media/image3.png)
  
    > [!Note]
    >
    > - By default, environments are automatically in the **frequent** cadence; creating and editing canvas apps will receive updates once a week. When apps are published, they will receive the corresponding runtime version.
    > - If you've chosen the **moderate** cadence for the environment, all creating and editing of canvas apps will receive updates once a month. When apps are published, they will receive the corresponding runtime version.


### Task 2: Control who can create and manage environments in the Power Platform admin center

1. Select the **Gear** icon in the upper-right corner of the **Microsoft Power Platform** site.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%201%20-%20Create%20and%20manage%20environments/media/image4.png)

1. Select **Power Platform settings**.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%201%20-%20Create%20and%20manage%20environments/media/image5.png)

1. Select **Add-on capacity assignments.**

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%201%20-%20Create%20and%20manage%20environments/media/image6.png)

1. Select **Only specific admins** and click **Save.**

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%201%20-%20Create%20and%20manage%20environments/media/image7.png)


### Task 3: Administration mode

You can set a sandbox, production, or trial (subscription-based) environment in administration mode so that only users with System Administrator or System Customizer security roles will be able to sign in to that environment. Administration mode is useful when you want to make operational changes and not have regular users affect your work, and not have your work affect end users (non-admins)

1. From the left-side menu, select **Manage** \> **Environments**, and then select your **Dev One** environment.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%201%20-%20Create%20and%20manage%20environments/media/image1.png)

1. On the **Details** page, click on **Edit**.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%201%20-%20Create%20and%20manage%20environments/media/image2.png)

1. Under **Administration mode**, toggle **Disabled** to **Enabled** and then select **Save**.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%201%20-%20Create%20and%20manage%20environments/media/image8.png)

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%201%20-%20Create%20and%20manage%20environments/media/image9.png)

1. On the **Details** page, click on **Edit**. **Disable** Administrative mode and **Save** it.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%201%20-%20Create%20and%20manage%20environments/media/image10.png)


## Exercise 2: Create a new custom security role

### Task 1 - Create a new custom security role that only has access to "Security Role" table

1. Open a new tab and navigate to +++https://make.powerapps.com+++. If required, sign in with your Office 365 tenant credentials.

1. Select your **Dev One** environment.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%201%20-%20Create%20and%20manage%20environments/media/image11.png)

1. Select your environment and click on **Settings** \> **Advanced Settings**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%201%20-%20Create%20and%20manage%20environments/media/image12.png)

1. **Dynamics 365** opens in separate tab. Click on **Settings \> Options.**

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%201%20-%20Create%20and%20manage%20environments/media/image13.png)

1. In the **General** tab, scroll down to the bottom and select the **user information** link.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%201%20-%20Create%20and%20manage%20environments/media/image14.png)

1. On the user information page select the different tabs, such as **Summary**, **Details**, or **Administration** to see details about your profile.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%201%20-%20Create%20and%20manage%20environments/media/image15.png)

1. Go back to **Power Platform admin center** tab. From the left-side menu, select **Manage** \> **Environments**, and then select your **Dev One** environment.

1. Select the **Gear** icon in the upper-right corner

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%201%20-%20Create%20and%20manage%20environments/media/image1.png)

1. Select **Settings**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%201%20-%20Create%20and%20manage%20environments/media/image16.png)

1. Click on **Users + permissions \> Security roles.**

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%201%20-%20Create%20and%20manage%20environments/media/image17.png)

1. Click on **New role.**

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%201%20-%20Create%20and%20manage%20environments/media/image18.png)

1. In the **Role Name** field, enter a name for the new role - **Security update**. In the **Business unit** field, select the business unit the role belongs to. Select **Save**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%201%20-%20Create%20and%20manage%20environments/media/image19.png)

1. Scroll down to the **Table** list and set the **Security Role** table privileges as follows. Click on **Save and Close** button.

    **Create**: Business Unit

    **Read**: Organization

    **Write**: Business Unit

    **Delete**: Business Unit

    **Append**: Business Unit

    **Append** **To**: Business Unit

    **Assign**: Business Unit

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%201%20-%20Create%20and%20manage%20environments/media/image20.png)


### Task 2: Assign the new security role to an administrative user

1. Click on **Settings** on top navigation.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%201%20-%20Create%20and%20manage%20environments/media/image21.png)

1. Click on **Users + permissions - \> Users**.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%201%20-%20Create%20and%20manage%20environments/media/image22.png)

1. Select an administrative user - **MOD Administrator** and then choose **Manage Security roles**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%201%20-%20Create%20and%20manage%20environments/media/image23.png)

1. Select the new security role - **Security update** which was created above and then **Save** it.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%201%20-%20Create%20and%20manage%20environments/media/image24.png)

1. Click on **Save** to confirm the role assignment.

    ![A screenshot of a computer error Description automatically generated](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%201%20-%20Create%20and%20manage%20environments/media/image25.png)


## Summary

In this lab, you learnt how to restrict environment creation and management to admins from the Power Platform Admin Center. You also learnt how to create security roles, give the privileges and assign it to an administrative user.
