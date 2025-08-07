**Lab 0: Set up lab environment**

**Estimated Duration:** 10 min

**Objective:** In this lab, you will acquire Power Apps trial license.
You will also add users and assign licenses to them at the same time.

### **Task 1: Assign** **Power Apps trial license** 

1.  Open a web browser on your VM and go to
    +++<https://powerapps.microsoft.com/en-us/free/>+++.

> ![](./media/image1.png)

2.  Select **Start free**.

> ![A person with his arms crossed Description automatically
> generated](./media/image2.png)

3.  Enter your **Office 365 admin credential**, check the checkbox to
    **accept the agreement** and click on **Start your free trial**.

> ![](./media/image3.png)

4.  Enter **password of your Office 365 tenant id** and then select
    **Sign in**.

> ![](./media/image4.png)

5.  Select **Yes** on **Stay signed in?** pop-up window.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image5.png)

6.  You can now see **Home page of Power Apps.** From the environment
    selector, select the developer environment – **Dev One** which is
    created for you.

> ![](./media/image6.png)

7.  Open the new tab and go to Power Platform admin center by navigating
    to +++<https://admin.powerplatform.microsoft.com>+++ and if
    required, sign in using your given Office 365 admin tenant
    credentials. Close the pop-up that says, ‘Welcome to the new Power
    Platform admin center’.

> ![](./media/image7.png)

8.  From the left navigation pane, select **Manage** \> **Environments**
    and then you can see, **Dev One** is your Dataverse environment.

> ![](./media/image8.png)

**Task 2: Create Microsoft 365 Users**

1.  Open **Import_Users_Contoso.csv** file from **C:\Labfiles** folder
    on your Lab VM.

2.  Under the **Username** column, update the tenant name to reflect
    your Office 365 tenant name for each user in the list and then save
    as a CSV format file.

> E.g. if your Office 365 tenant is <admin@LODSA7xx479.onmicrosoft.com>,
> your domain would be LODSA7xx479.
>
> eg : <brookeg@LODSA7xx479.onmicrosoft.com>

3.  Navigate to the Microsoft 365 admin center using
    +++[https://admin.microsoft.com+++](https://admin.microsoft.com+++/)

4.  From the left navigation, select **Users** \> **Active users** page,
    click **Add multiple users**.

> ![](./media/image9.png)

5.  On the Upload a CSV file with user info pane, select **I’d like to
    upload a CSV with user information** and then click **Browse**.

> ![](./media/image10.png)

6.  In the Open dialog box, navigate **C:\Labfiles\\
    Import_Users_Contoso.csv** and click **Open**.

> ![A screenshot of a computer Description automatically
> generated](./media/image11.png)

7.  Once the CSV file passed verification, click **Next**.

> ![](./media/image12.png)
>
> **NOTE**: If you receive an error message, review your CSV file for
> errors, and fix them

8.  On the Licenses pane, select all the license check boxes and
    click **Next**.

> ![](./media/image13.png)

9.  On the **Review and finish adding multiple users** pane, click **Add
    users**.

> ![](./media/image14.png)

10. On the **You added 11 users** pane, click **Close**.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image15.png)

11. On the **Active users** page, select all the new users, (except MOD
    Admin) then click on **Reset password**.

> ![](./media/image16.png)

12. To reset the same password for all the users, uncheck all check
    boxes and enter password as : +++Pa$$w0rd@124+++ and then click
    on **Reset password**.

> ![](./media/image17.png)

13. On the **Reset password** pane, click **Close**.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image18.png)
>
> **Summary:** In this lab, you acquired Power Apps trial license and
> also added users from the Microsoft 365 admin center.
