# **Lab 4: Configure Governance Controls for your Copilot Studio Agents**

**Estimated time:** 60 min

**Objective**: In this lab, you will learn how to create security group
and add members to the security group from the Microsoft 365 admin
center, import and share agent solutions, and enforce governance
policies using the Power Platform admin center. You will also learn how
to configure data access and deploy agents to ensure secure, scalable.

## **Exercise 1: Control user access to environments: security groups and licenses**

### **Task 1: Create a security group and add members to the security group**

1.  Open new tab in the same browser and navigate to **Microsoft 365
    admin
    center** using [**https://admin.microsoft.com**](urn:gd:lg:a:send-vm-keys).
    Sign in with your Office 365 tenant credentials.

2.  Select **Teams & groups** \> **Active teams & groups**.

> ![](./media/image1.png)

3.  Select **Security group** tab and then select **+Add a security
    group**.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image2.png)

4.  Add the group Name: [**PPS-security**
    and** Description:**](urn:gd:lg:a:send-vm-keys) Power Platform
    security group and then click **Next**.

> ![](./media/image3.png)

5.  Click on **Create group** button.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image4.png)

6.  Click on **Close** button to close the window.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image5.png)

7.  Select the PPS-security group you created.

> ![](./media/image6.png)

8.  Select **Members** tab and then click on **View all and managed
    members** hyper link.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image7.png)

9.  Click on **+ Add members**.

> ![](./media/image8.png)

10. Select the first three users (For example here, Brooke, Connie and
    Jacob) to add to the security group and then select **Add(3).**

> ![](./media/image9.png)

11. **Close** the ‘Members’ pane to return to the **Groups** list.

> ![A screenshot of a group of members AI-generated content may be
> incorrect.](./media/image10.png)

12. You have completed this task, please do not close the tab and 
    proceed ahead with the next task.

**Task 2: Associate a security group with a Dataverse environment**

1.  Open new tab and navigate to Power Platform admin center
    using [**https://admin.powerplatform.microsoft.com**](urn:gd:lg:a:send-vm-keys) and
    if required, sign in with your Office 365 tenant credentials. 

2.  In the navigation pane, select **Manage \>** **Environments**, and
    then select **+New**.

> ![](./media/image11.png)

3.  On the New environment window, enter the following information.

> **Name:** Test
>
> **Region**: United States – Default
>
> **Type**: Trial
>
> **Add a Dataverse data store**: Yes
>
> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image12.png)
>
> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image13.png)

4.  Keep the **Language** as **English (United States)**, **Currency**
    as **USD** and then click on **+** **Select**.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image14.png)

5.  Under the **Restricted access**, select **PPS-Security** and then
    select **Done**.

> ![](./media/image15.png)

6.  You can see under Security group, **PPS-security** group is added
    and then select **Save**.

> ![](./media/image16.png)

## **Exercise 2: Create an agent**

### **Task 1: Create an agent**

1.  Navigate to [Microsoft Copilot
    Studio](https://copilotstudio.microsoft.com/) using
    <https://copilotstudio.microsoft.com/>. Sign in with your Office 365
    Admin tenant credentials.

2.  From the environment selector, select **Test** environment that has
    the tables you created in the previous exercise.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image17.png)

3.  Select **Create** from the left navigation pane and select the **New
    agent** tile.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image18.png)

4.  Select **Skip to configure** in the top-right corner of the agent
    creation screen.

> ![](./media/image19.png)

5.  In the **Name** text box, enter **Real Estate Booking Service.**

> ![Screenshot of Details pane in Copilot Studio
> portal.](./media/image20.png)

6.  In the **Description** text box, enter **Create bookings for real
    estate properties.**

7.  In the **Instructions** text box, enter **Speak courteously and
    mimic the behavior of a real estate agent.** Select **Create**.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image21.png)

### **Task 2: Configure Security**

1.  Select **Settings** in the top-right of the **Real Estate Booking
    Service** agent's screen.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image22.png)

2.  Select the **Security** tab and then select
    the **Authentication** tile.

> ![](./media/image23.png)

3.  Select **No authentication** and select **Save**.

> ![](./media/image24.png)

4.  Select **Save** in the **Save this configuration?** window.

> ![](./media/image25.png)

5.  Close the **Settings** menu and return to your **Real Estate Booking
    Service** agent.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image26.png)

## **Exercise 3: Configure DLP to block Power Platform connectors in the Power Platform admin center**

**Task 1: Create a policy**

1.  Navigate to Power Platform admin center
    using [**https://admin.powerplatform.microsoft.com**](urn:gd:lg:a:send-vm-keys) and
    if required, sign in with your Office 365 tenant credentials. 

2.  From the left navigation pane, select **Security**.
    Under **Security**, select **Data and privacy** then select **Data
    policy** tile.

> ![](./media/image27.png)

3.  To create a new policy, select **+New policy**.

> ![](./media/image28.png)

4.  Enter name of the policy **- PP-Connector Policy** and
    click **Next**.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image29.png)

5.  In the search box, type **MSN**, select **more actions** (3 dots)
    for **MSN Weather** connector and then select **Block**.

> ![](./media/image30.png)

6.  Select **Blocked** tab, you can see **MSN Weather** connector which
    you have just blocked. Select **Next**.

> ![](./media/image31.png)

7.  Do not add any connectors and click on **Next**.

> ![](./media/image32.png)

8.  In **Scope**, select **Add multiple environments** and then
    click **Next.**

> ![](./media/image33.png)

9.  Select your **Test** trial environment and then click on **+Add to
    policy**.

> ![](./media/image34.png)

10. Select **Added to policy** tab and then click **Next**.

> ![](./media/image35.png)

11. **Review** the policy and then click on **Create policy**.

> ![](./media/image36.png)

12. Your **Policy** got created.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image37.png)
>
> **Task 2: Confirm policy enforcement**
>
> You can confirm that this connector is being used in the DLP policy
> from Copilot Studio:

1.  Go back to Copilot Studio portal. Ensure that You are in **Test**
    environment where the DLP policy is applied.

> ![](./media/image38.png)

2.  Select **Agents** from the left navigation pane. Open **Real Estate
    Booking Service** agent.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image39.png)

3.  Select **Topics** tab. Select **Custom(4)** tab.

> ![](./media/image40.png)

4.  Select **+ Add a topic** \> **Add from description with Copilot**.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image41.png)

5.  Enter following Information and then select **Create**.

> **Name your topic:** Property Viewings Scheduling
>
> **Create a topic to...:** This topic would allow users to schedule
> property viewings directly through the chatbot, streamlining the
> booking process and enhancing the user experience
>
> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image42.png)

6.  For a better view, close the **Edit with Copilot** pane.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image43.png)

7.  At the end of the last node select **+** icon to add new node.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image44.png)

8.  Select **Add a tool** node and then select **Connector** tab.

> ![](./media/image45.png)

9.  In the node's properties, select **Connectors** and choose your
    connection. Save your topic.

> ![](./media/image46.png)

10. Click on **Not connected** and select **Create new connection**.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image47.png)

11. Select **Create**.

> **Note**: If asked, sign in with the given Office 365 tenant
> credentials.
>
> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image48.png)

12. You can see the message as Connection creation has been blocked by
    Data Loss Prevention (DLP) policy ‘PP-Connector policy’. This shows
    your policy is enforced.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image49.png)

## **Exercise 4: Import and Export a Copilot Studio Agent Solution**

**Task 1: Export an Agent into Copilot Studio**

1.  In Copilot Studio, select the menu icon (**…**) on the side
    navigation pane, and then select **Solutions**.

![](./media/image50.png)

2.  Select **+New solution**.

![](./media/image51.png)

3.  Enter the following information and then select **+New publisher**.

**Display name**: Real Estate

**Name**: RealEstate

![](./media/image52.png)

4.  On the **New publisher** pane, enter the following information and
    then select **Save**.

**Display name:** Booking Service

**Name:** BookingService

**Prefix**: book

![](./media/image53.png)

5.  Now on the **New solution** pane, a new publisher name, i.e.
    **Booking Service**, has been selected already. If not, then select
    it from the drop-down list.

![](./media/image54.png)

6.  Now, you will be in **Real Estate** solution.

![](./media/image55.png)

7.  Click on the **Add existing** drop-down then select **Agent** \>
    **Agent**.

![](./media/image56.png)

8.  Select **Real Estate Booking Service** agent and then click on the
    **Add** button.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image57.png)

9.  After adding the agent to the solution, select **Publish all
    customizations**.

![](./media/image58.png)

10. When you see the message ‘**Publish all customizations succeeded’**
    then click on the back arrow to go back to the **Agents** page.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image59.png)

11. On the Copilot Studio portal, select Agents from the left navigation
    pane. Click the **ellipsis (...)** icon on the **Real Estate Booking
    Service Agent** and select **Export Agent**.

![](./media/image60.png)

12. In the **Agent Solution**, click the **ellipsis (...)** icon again
    and select **Export solution**.

![](./media/image61.png)

13. Click **Next** to proceed.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image62.png)

14. Select the **Unmanaged** option and then click on the **Export**
    button.

![](./media/image63.png)

15. You can see the given message, ‘Currently exporting solution’.

![A close-up of a text AI-generated content may be
incorrect.](./media/image64.png)

16. Once the export is complete, click on the **Download** button from
    the top. The agent will be downloaded to the **Downloads** folder in
    the VM.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image65.png)

> **Task 2: Import Agent into Copilot Studio**

1.  On the Copilot Studio portal, click on the **Environment selector**
    and select **Dev One** environment.

![](./media/image66.png)

2.  In Microsoft Copilot Studio, click on **Agents** from the left-hand
    menu and then click on the **Import Agent.**

![](./media/image67.png)

3.  In the top menu bar, click **Import** **solution**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image68.png)

4.  Click the **Browse** button and navigate to the Lab Files folder on
    the virtual machine.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image69.png)

5.  Select the **RealEstate solution** lab file from the Downloads
    folder on the VM, click on the **Open** button.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image70.png)

6.  Select **Next** to proceed.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image71.png)

7.  Click the **Import** button to import the agent solution.

![](./media/image72.png)

8.  After successful import, select the newly imported agent solution.
    Click on the **More commands** (3 dots).

9.  Click **Set preferred solution** from the top bar.

![](./media/image73.png)

10. Click **Apply** to confirm the selected solution.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image74.png)

**Task 3: Share Agent with Another User**

1.  Click on the **ellipsis (...)** icon on the **Contoso Agent** and
    select **Share**.

> ![](./media/image75.png)

2.  In the **New User** field, enter **Sara** and select the user **Sara
    Perez** from the dropdown.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image76.png)

3.  Click on the **Update** button to share the agent.

> ![](./media/image77.png)

4.  After successful sharing, click the **Close (X)** icon to exit the
    sharing window.

> ![](./media/image78.png)

## **Exercise 5: Configure Access and Deploy Copilot Studio Agent**

**Task 1: Configure Data Access for Specific Users**

1.  From the left-hand menu under **Copilot**, click **Settings**.

> ![](./media/image79.png)

2.  Go to the **Data Access** section and click on **Agent**.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image80.png)

3.  Choose **Specific users/group** option.

> ![](./media/image81.png)

4.  Enter and select **MOD Administrator** and **Sara Perez** users then
    click **Save** to apply access settings.

> ![](./media/image82.png)

**Task 2: Deploy Agent and Assign User**

1.  In the left menu under **Copilot**, click **Agent and Connectors**.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image83.png)

2.  In the Agent Inventory, search for **Microsoft 365**, then open the
    **Admin Agent**.

> ![](./media/image84.png)

3.  Click **Deploy** from the top options and then click on the **Next**
    button.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image85.png)
>
> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image86.png)

4.  Select on the **Just me** option, and then click on the **Next**
    button.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image87.png)

5.  Click **Next** again, then click on the **Finish deployment**
    button.

> ![](./media/image88.png)
>
> ![](./media/image89.png)

6.  Click **Done** to complete.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image90.png)

7.  To assign new user access, go to **Users**, then select **Deployed
    to**.

8.  Select **Specified user/group**,

> ![](./media/image91.png)

9.  Enter **Sara** and select the user, **Sara Perez**.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image92.png)

10. Click on the **Update** button to add new user.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image93.png)

11. Click the **X** on the top-right to close.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image94.png)

**Task 3: Test Microsoft 365 Admin Copilot Agent Functionality**

1.  Open a Microsoft Edge new tab and navigate to office 365 copilot
    <https://www.office.com/> then click on the **Sign in** button.

![](./media/image95.png)

2.  If asked, sign in with the given **Office 365** **Admin tenant
    credentials.**

![](./media/image96.png)

3.  On the left-hand menu, locate and click on the **Microsoft 365 Admin
    Agent**.

![](./media/image97.png)

**Note:** If the agent doesn’t appear immediately, wait a few minutes
for it to load.

4.  Click on the **“Learn admin tasks”** prompt to test the agent. Click
    the **Execute** button to run the prompt.

![](./media/image98.png)

5.  The prompt will run and return the results, confirming successful
    execution.

![](./media/image99.png)

**Summary**: In this lab, you learnt to create a security group, add
members and associate it with Dataverse environment. You created a DLP
policy and examined its impact on the agent. You imported agent from
trial environment to developer environment and shared that with the
user.
