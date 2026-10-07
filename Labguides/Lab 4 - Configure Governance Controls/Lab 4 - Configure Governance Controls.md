<!--
lab:
  title: 'Lab 4: Configure Governance Controls for your Copilot Studio Agents'
  description: In this lab, you will learn how to create security group
and add members to the security group from the Microsoft 365 admin
center, import and share agent solutions, and enforce governance
policies using the Power Platform admin center. You will also learn how
to configure data access and deploy agents to ensure secure, scalable.
  duration: 60 minutes
  level: 200
  islab: true
  primarytopics:
    - Office 365
-->

# Lab 4: Configure Governance Controls for your Copilot Studio Agents

**Estimated time:** 60 min

### Objective

In this lab, you will learn how to create security group and add members to the security group from the Microsoft 365 admin center, import and share agent solutions, and enforce governance policies using the Power Platform admin center. You will also learn how to configure data access and deploy agents to ensure secure, scalable.

## Exercise 1: Control user access to environments: security groups and licenses

### Task 1: Create a security group and add members to the security group

1. Open new tab in the same browser and navigate to **Microsoft 365 admin center** using [**https://admin.microsoft.com**](urn:gd:lg:a:send-vm-keys). Sign in with your Office 365 tenant credentials.

1. Select **Teams & groups** \> **Active teams & groups**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image1.png)

1. Select **Security group** tab and then select **+Add a security group**.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image2.png)

1. Add the group Name: [+++PPS-security+++ and** Description:**](urn:gd:lg:a:send-vm-keys) Power Platform security group and then click **Next**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image3.png)

1. Click on **Create group** button.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image4.png)

1. Click on **Close** button to close the window.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image5.png)

1. Select the PPS-security group you created.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image6.png)

1. Select **Members** tab and then click on **View all and managed members** hyper link.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image7.png)

1. Click on **+ Add members**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image8.png)

1. Select the first three users (For example here, Brooke, Connie and Jacob) to add to the security group and then select **Add(3).**

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image9.png)

1. **Close** the ‘Members’ pane to return to the **Groups** list.

    ![A screenshot of a group of members AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image10.png)

1. You have completed this task, please do not close the tab and proceed ahead with the next task.


### Task 2: Associate a security group with a Dataverse environment

1. Open new tab and navigate to Power Platform admin center using [**https://admin.powerplatform.microsoft.com**](urn:gd:lg:a:send-vm-keys) and if required, sign in with your Office 365 tenant credentials.

1. In the navigation pane, select **Manage \>** **Environments**, and then select **+New**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image11.png)

1. On the New environment window, enter the following information.

    **Name:** Test

    **Region**: United States – Default

    **Type**: Trial

    **Add a Dataverse data store**: Yes

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image12.png)

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image13.png)

1. Keep the **Language** as **English (United States)**, **Currency** as **USD** and then click on **+** **Select**.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image14.png)

1. Under the **Restricted access**, select **PPS-Security** and then select **Done**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image15.png)

1. You can see under Security group, **PPS-security** group is added and then select **Save**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image16.png)


## Exercise 2: Create an agent

### Task 1: Create an agent

1. Navigate to [Microsoft Copilot Studio](https://copilotstudio.microsoft.com/) using <https://copilotstudio.microsoft.com/>. Sign in with your Office 365 Admin tenant credentials.

1. From the environment selector, select **Test** environment that has the tables you created in the previous exercise.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image17.png)

1. Select **Create** from the left navigation pane and select the **New agent** tile.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image18.png)

1. Select **Skip to configure** in the top-right corner of the agent creation screen.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image19.png)

1. In the **Name** text box, enter **Real Estate Booking Service.**

    ![Screenshot of Details pane in Copilot Studio portal.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image20.png)

1. In the **Description** text box, enter **Create bookings for real estate properties.**

1. In the **Instructions** text box, enter **Speak courteously and mimic the behavior of a real estate agent.** Select **Create**.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image21.png)


### Task 2: Configure Security

1. Select **Settings** in the top-right of the **Real Estate Booking Service** agent's screen.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image22.png)

1. Select the **Security** tab and then select the **Authentication** tile.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image23.png)

1. Select **No authentication** and select **Save**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image24.png)

1. Select **Save** in the **Save this configuration?** window.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image25.png)

1. Close the **Settings** menu and return to your **Real Estate Booking Service** agent.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image26.png)


## Exercise 3: Configure DLP to block Power Platform connectors in the Power Platform admin center

### Task 1: Create a policy

1. Navigate to Power Platform admin center using [**https://admin.powerplatform.microsoft.com**](urn:gd:lg:a:send-vm-keys) and if required, sign in with your Office 365 tenant credentials.

1. From the left navigation pane, select **Security**. Under **Security**, select **Data and privacy** then select **Data policy** tile.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image27.png)

1. To create a new policy, select **+New policy**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image28.png)

1. Enter name of the policy **- PP-Connector Policy** and click **Next**.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image29.png)

1. In the search box, type +++MSN+++, select **more actions** (3 dots) for **MSN Weather** connector and then select **Block**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image30.png)

1. Select **Blocked** tab, you can see **MSN Weather** connector which you have just blocked. Select **Next**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image31.png)

1. Do not add any connectors and click on **Next**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image32.png)

1. In **Scope**, select **Add multiple environments** and then click **Next.**

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image33.png)

1. Select your **Test** trial environment and then click on **+Add to policy**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image34.png)

1. Select **Added to policy** tab and then click **Next**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image35.png)

1. **Review** the policy and then click on **Create policy**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image36.png)

1. Your **Policy** got created.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image37.png)

    **Task 2: Confirm policy enforcement**

    You can confirm that this connector is being used in the DLP policy from Copilot Studio:

1. Go back to Copilot Studio portal. Ensure that You are in **Test** environment where the DLP policy is applied.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image38.png)

1. Select **Agents** from the left navigation pane. Open **Real Estate Booking Service** agent.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image39.png)

1. Select **Topics** tab. Select **Custom(4)** tab.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image40.png)

1. Select **+ Add a topic** \> **Add from description with Copilot**.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image41.png)

1. Enter following Information and then select **Create**.

    > **Name your topic:** Property Viewings Scheduling
    >
    > **Create a topic to...:** This topic would allow users to schedule
    > property viewings directly through the chatbot, streamlining the
    > booking process and enhancing the user experience

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image42.png)

1. For a better view, close the **Edit with Copilot** pane.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image43.png)

1. At the end of the last node select **+** icon to add new node.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image44.png)

1. Select **Add a tool** node and then select **Connector** tab.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image45.png)

1. In the node's properties, select **Connectors** and choose your connection. Save your topic.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image46.png)

1. Click on **Not connected** and select **Create new connection**.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image47.png)

1. Select **Create**.

    >[!Note] If asked, sign in with the given Office 365 tenant credentials.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image48.png)

1. You can see the message as Connection creation has been blocked by Data Loss Prevention (DLP) policy ‘PP-Connector policy’. This shows your policy is enforced.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image49.png)


## Exercise 4: Import and Export a Copilot Studio Agent Solution

### Task 1: Export an Agent into Copilot Studio

1. In Copilot Studio, select the menu icon (**…**) on the side navigation pane, and then select **Solutions**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image50.png)

1. Select **+New solution**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image51.png)

1. Enter the following information and then select **+New publisher**.

    **Display name**: Real Estate

    **Name**: RealEstate

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image52.png)

1. On the **New publisher** pane, enter the following information and then select **Save**.

    **Display name:** Booking Service

    **Name:** BookingService

    **Prefix**: book

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image53.png)

1. Now on the **New solution** pane, a new publisher name, i.e. **Booking Service**, has been selected already. If not, then select it from the drop-down list.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image54.png)

1. Now, you will be in **Real Estate** solution.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image55.png)

1. Click on the **Add existing** drop-down then select **Agent** \> **Agent**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image56.png)

1. Select **Real Estate Booking Service** agent and then click on the **Add** button.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image57.png)

1. After adding the agent to the solution, select **Publish all customizations**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image58.png)

1. When you see the message ‘**Publish all customizations succeeded’** then click on the back arrow to go back to the **Agents** page.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image59.png)

1. On the Copilot Studio portal, select Agents from the left navigation pane. Click the **ellipsis (...)** icon on the **Real Estate Booking Service Agent** and select **Export Agent**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image60.png)

1. In the **Agent Solution**, click the **ellipsis (...)** icon again and select **Export solution**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image61.png)

1. Click **Next** to proceed.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image62.png)

1. Select the **Unmanaged** option and then click on the **Export** button.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image63.png)

1. You can see the given message, ‘Currently exporting solution’.

    ![A close-up of a text AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image64.png)

1. Once the export is complete, click on the **Download** button from the top. The agent will be downloaded to the **Downloads** folder in the VM.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image65.png)

    > **Task 2: Import Agent into Copilot Studio**

1. On the Copilot Studio portal, click on the **Environment selector** and select **Dev One** environment.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image66.png)

1. In Microsoft Copilot Studio, click on **Agents** from the left-hand menu and then click on the **Import Agent.**

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image67.png)

1. In the top menu bar, click **Import** **solution**.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image68.png)

1. Click the **Browse** button and navigate to the Lab Files folder on the virtual machine.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image69.png)

1. Select the **RealEstate solution** lab file from the Downloads folder on the VM, click on the **Open** button.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image70.png)

1. Select **Next** to proceed.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image71.png)

1. Click the **Import** button to import the agent solution.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image72.png)

1. After successful import, select the newly imported agent solution. Click on the **More commands** (3 dots).

1. Click **Set preferred solution** from the top bar.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image73.png)

1. Click **Apply** to confirm the selected solution.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image74.png)


### Task 3: Share Agent with Another User

1. Click on the **ellipsis (...)** icon on the **Contoso Agent** and select **Share**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image75.png)

1. In the **New User** field, enter +++Sara+++ and select the user **Sara Perez** from the dropdown.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image76.png)

1. Click on the **Update** button to share the agent.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image77.png)

1. After successful sharing, click the **Close (X)** icon to exit the sharing window.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image78.png)


## Exercise 5: Configure Access and Deploy Copilot Studio Agent

### Task 1: Configure Data Access for Specific Users

1. From the left-hand menu under **Copilot**, click **Settings**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image79.png)

1. Go to the **Data Access** section and click on **Agent**.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image80.png)

1. Choose **Specific users/group** option.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image81.png)

1. Enter and select **MOD Administrator** and **Sara Perez** users then click **Save** to apply access settings.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image82.png)


### Task 2: Deploy Agent and Assign User

1. In the left menu under **Copilot**, click **Agent and Connectors**.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image83.png)

1. In the Agent Inventory, search for **Microsoft 365**, then open the **Admin Agent**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image84.png)

1. Click **Deploy** from the top options and then click on the **Next** button.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image85.png)

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image86.png)

1. Select on the **Just me** option, and then click on the **Next** button.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image87.png)

1. Click **Next** again, then click on the **Finish deployment** button.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image88.png)

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image89.png)

1. Click **Done** to complete.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image90.png)

1. To assign new user access, go to **Users**, then select **Deployed to**.

1. Select **Specified user/group**,

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image91.png)

1. Enter +++Sara+++ and select the user, **Sara Perez**.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image92.png)

1. Click on the **Update** button to add new user.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image93.png)

1. Click the **X** on the top-right to close.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image94.png)


### Task 3: Test Microsoft 365 Admin Copilot Agent Functionality

1. Open a Microsoft Edge new tab and navigate to office 365 copilot <https://www.office.com/> then click on the **Sign in** button.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image95.png)

1. If asked, sign in with the given **Office 365** **Admin tenant credentials.**

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image96.png)

1. On the left-hand menu, locate and click on the **Microsoft 365 Admin Agent**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image97.png)

    >[!Note] If the agent doesn’t appear immediately, wait a few minutes for it to load.

1. Click on the **“Learn admin tasks”** prompt to test the agent. Click the **Execute** button to run the prompt.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image98.png)

1. The prompt will run and return the results, confirming successful execution.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%204%20-%20Configure%20Governance%20Controls/media/image99.png)


## Summary

In this lab, you learnt to create a security group, add members and associate it with Dataverse environment. You created a DLP policy and examined its impact on the agent. You imported agent from trial environment to developer environment and shared that with the user.
