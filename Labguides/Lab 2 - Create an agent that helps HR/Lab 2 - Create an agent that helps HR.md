<!--
lab:
  title: 'Lab 2: Create an agent that helps HR with onboarding a new employee'
  description: In this lab, you will learn how to automate the employee
onboarding process at by building the Agent.
  duration: 60 minutes
  level: 100
  islab: true
-->

# Lab 2: Create an agent that helps HR with onboarding a new employee

**Estimated Duration**: 60 min

### Objective

In this lab, you will learn how to automate the employee onboarding process at by building the Agent. As a member of the HR team, you are building an HR agent to simplify the employee onboarding process. You will create an agent that can perform the following activities:
- Provide general information and answer queries that relate to employee
  onboarding.

- Submit a request automatically to onboard a new employee through the
  system.

- Send an onboarding request approval email automatically to the hiring
  manager that includes tasks, such as procuring a laptop, setting up an email account, and other onboarding essentials.

- Analyze the response for approval after the hiring manager responds to
  the email. Then, based on the response, take action to send an email to the IT/procurement team to procure a laptop and set up their access.

- Wait for the IT/procurement team to confirm procurement and then email
  the new employee with onboarding instructions.


## Exercise 1: Create the autonomous agent

### Task 1: Create a custom table in Dataverse

A Dataverse table named Employee Record is used to store all employee onboarding details collected by the chatbot.

1. Go to the Power Apps maker portal using +++https://make.powerapps.com/+++ and if required sign in with the given Office 365 Admin tenant credentials.

1. Open the **Employee details** excel sheet located in the VM **C:\Labfiles** folder. Enter your email address under the **Email** column and enter given Mod Admin’s email id under the **ManagerEmail** column for all the entries. Save the changes and close the excel sheet.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image1.png)

1. Navigate to **Power Apps** > **Tables** > select **Create new tables** from the **New table** dropdown.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image2.png)

1. From Choose an option to create tables window select **Import an Excel file or CSV**.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image3.png)

1. Click on **Select from device** \> select and open your **Employee details** Excel file

1. Once the file is loaded successfully, click **Import.**

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image4.png)

1. Select the table and click on **View data.**

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image5.png)

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image6.png)

1. Select the column \> **edit column** and set it to the **Text** type.

1. Configure the table:

    > Employee ID: **Text**
    >
    > Employee Name: +++Text+++
    >
    > Email: **Text**
    >
    > Department: **Text**
    >
    > Designation: **Text**
    >
    > Date of Joining: **Text**
    >
    > Manager’s email: **Text**
    >
    >[!Note] This table acts as the central database for storing all relevant employee onboarding data.
    >
    >[!Note] In my case the employee details table saved as employee record.

1. Again, select **Save and exit** on the **Done working** pop-up.

    ![A screenshot of a computer screen AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image7.png)


### Task 2: Create an Autonomous Onboarding gent

1. To create a new agent in Copilot Studio, sign in to Copilot Studio using <https://go.microsoft.com/fwlink/?LinkId=2107702> with the given Office 365 Admin tenant credentials. Complete the authentication process and then select **Sign In**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image8.png)

1. Fill up the following required information and then select **Get Started**.

    > **Country or Region** – United States
    >
    > **Job title** – Your job title
    >
    > **Business phone number** – Your phone number
    >

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image9.png)

1. Under Confirmation details step, select **Get Started**.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image10.png)

1. Select United States as **Country or Region** and then select **Get Started**.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image11.png)

1. Click on the **Environment selector** and then select **Dev One** environment.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image12.png)

1. Select **Skip** on the pop-up that states **Welcome to Copilot Studio!**.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image13.png)

1. Select **Create** in the left navigation pane then select the **New Agent** box.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image14.png)

1. From the **Create New Agent** screen, select **Skip to configure** to create the agent manually you can choose from two methods to create an agent.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image15.png)

1. The **Create New Agent** screen has three fields: **Name**, **Description**, and **Instructions**. Enter the following information in these fields:

    - **Name** - Employee Onboarding Agent
    - **Description** - An agent developed to simplify the employee
    onboarding process.

    - **Instructions** - You are an agent responsible for employee
    onboarding. After you receive the onboarding request from HR, validate it and send the employee details to the hiring manager for approval. When the hiring manager approves it, forward the information to the IT and procurement teams so they can complete their respective tasks. After they finish their tasks, send the onboarding confirmation along with the onboarding instructions to the employee.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image16.png)


1. Select the **Create** button to create the agent.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image17.png)


### Task 3: Enhance agent intelligence

You can enhance the **Employee Onboarding Agent** that you created in the previous task by adding knowledge and intelligence to the agent.

1. To add generative reasoning to the agent, in the **Orchestration** section, turn on **Use generative AI to determine how best to respond to users and events**. This selection allows generative AI reasoning to respond to questions from different users.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image18.png)

    >[!Note] In addition to enhancing knowledge from generative AI, you can use the **Knowledge** section to add your enterprise knowledge base.

1. To upload your resources and create a knowledge base, select the **Add knowledge** button to ensure that your agent has the information for accurate and efficient responses.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image19.png)

1. In the **Add knowledge** wizard, select **Dataverse** to connect the table.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image20.png)

1. On Step **1 of 3: Select Dataverse tables** wizard page, follow these steps to connect the table from Dataverse:

    - In the search bar, search for the table named **Employee Record**.
    - From the list of tables that contain **Employee Record** in their
    names, select the table that you want to connect to. You can select multiple tables as a knowledge source.

    - Click **Add** to continue.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image21.png)

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image22.png)


## Exercise 2: Create the Agent flow

### Task 1: Add When an agent calls the flow

1. Go to Copilot Studio Agent overview page.

1. Navigate to **Flows** \> **+ New Agent flows** \> select **Instant cloud flows**

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image23.png)

1. Click on **Add a trigger** button to add triggers to the flow

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image24.png)

1. Click on the trigger button, search and select **When an agent calls the flow** trigger.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image25.png)

1. Configure “**When an agent calls the flow”** trigger by following the steps below.

1. Add the following input parameters to the flow.

    > Employee ID
    >
    > Employee Name
    >
    > Email
    >
    > Department
    >
    > Designation
    >
    > Date of Joining
    >
    > Manager’s email

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image26.png)

1. Click on collapse icon **\<\<** to save the changes.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image27.png)


### Task 2: Add “Add a new row” trigger

This trigger refers to potential enhancements where you might want to act upon changes to the Dataverse table.

1. Click on **Add action +sign** after when an agent calls the flow trigger.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image28.png)

1. Search and select **Add a new row** trigger.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image29.png)

1. Configure **Add a new row** action.

    > You will use the **Dataverse connector** to add employee responses
    > into the Employee Record table.
    >
    > **Action:** Add a new row
    >
    > **Table name**: Employee record  
    > **Details to map**: Map dynamic variables to each parameter.
    >
    > Employee ID
    >
    > Employee Name
    >
    > Email
    >
    > Department
    >
    > Designation
    >
    > Date of Joining
    >
    > Manager’s email
    >
    >[!Note] This step ensures all collected data is stored properly in the Dataverse table.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image30.png)

1. Click on collapse option to close the configuration window.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image31.png)


### Task 3: Add “Send an email (V2)” Trigger (For HR)

You will send a notification to the HR team to inform them that a new employee onboarding request has been submitted.

1. Trigger an email notification to the HR team once a new row is added.

1. Click on **Add new action node +,** search and select **Send an email** trigger

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image32.png)

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image33.png)

1. Configure the “**Send an email**” trigger

    > **To:** HR (MOD Admin email – Start typing Admin and select MOD Admin
    ```
    from the suggestion)
    **Subject:** New Employee Onboarding Request
    **Body:**
    Dear HR,
    Please start the onboarding process for the new employee:
    Name: /Employee Name *{Select **Employee Name** from Dynamic content}*
    Department: /Department *{Select **Department** from Dynamic content}*
    Start Date: /Date of joining <Select **Date of joining** from Dynamic
    content>
    Regards,
    ```

    HR Onboarding Assistant

    >[!Note] Set up the **dynamic value** for each parameter using triggerBody.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image34.png)


### Task 4: Add “Send an email” Trigger (For Employee)

You now configure another email step to acknowledge the employee about their onboarding.

1. Again, add **Send an email** action to send the confirmation email to the respective employees for their onboarding request

1. Click on add a new action “**+”** sign to add Send an email trigger

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image35.png)

1. Configure send an email action

    **To**: +++Your+++ email id (emp email)

    **Subject**: Welcome to the Team

    **Body**: Hello

    Congratulations! You have been successfully onboarded at TF.

    Start Date:*{Select **Date of joining** from Dynamic content}*

    Department:*{Select **Department** from Dynamic content}*

    Welcome aboard!

    Regards,

    Contoso Onboarding Assistant

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image36.png)

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image37.png)

1. After all the necessary actions are added click on **Save draft** and **Publish**.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image38.png)

1. Once both email actions and Dataverse actions are configured, click **Save** and then **Publish** the flow to make it available to the Copilot agent.


### Task 5: Rename the flow

Rename the flow from untitled to Onboarding agent flow

1. Open overview page of the **flow**, click on **Edit** button to view the details

1. Change the flow name to Onboarding agent and Save

    **Name**: onboarding agent

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image39.png)

    >[!Note] This name will be referenced inside your chatbot topic.


## Exercise 3: Test the flow

Manually test the flow from Power Automate or from within Copilot Studio to verify:
- Emails are sent
- Data is added to Dataverse


1. Click on **Test** icon on the right corner of the window , select **Test manually.**

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image40.png)

1. Provide the demo inputs and click **Run flow.**

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image41.png)

1. Successful run triggers an email to HR, employee confirmation mail, and logs the input in the Employee Record table of +++Dataverse+++.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image42.png)

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image43.png)

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image44.png)


## Exercise 4: Create Agent Topics

### Task 1: Create Employee Details Topic

1. Go to **Employee Onboarding Agent** overview page.

1. Navigate to Topics tab, click **+ Add a topic** and choose **From blank** to start a new topic manually.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image45.png)

1. Configure the topic:

    **Name:** Employee details **Description:** An agent developed to simplify the employee onboarding process.


### Phrases:
    - Onboarding request
    - Help me onboard to TF

    > These trigger phrases allow users to begin the conversation naturally.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image46.png)

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image47.png)


1. Add the below question nodes to collect user input.

1. **Question node 1:**

    **Question:** Enter your full name? **Identify as:** User’s entire response **Var:** empname

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image48.png)

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image49.png)

1. **Question node 2:**

    **Question:** What is your employee ID? **Identify as:** User’s entire response **Var:** empId

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image50.png)

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image51.png)

1. **Question node 3:**

    **Question:** Provide your email Id **Identify as:** User’s entire response **Var:** email

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image52.png)

1. **Question node 4:**

    **Question:** Enter the department name **Identify as:** User’s entire response **Var:** dept

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image53.png)

1. **Question node 5:**

    **Question:** Enter the date of joining **Identify as:** User’s entire response **Var:** doj

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image54.png)

1. **Question node 6:**

    **Question:** Enter the designation **Identify as:** User’s entire response **Var:** dsgn

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image55.png)

1. **Question node 7:**

    **Question:** Enter the Manager’s email address **Identify as:** User’s entire response **Var:** mgremail

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image56.png)

    >[!Note] These questions collect the required data to be sent to Power Automate.

1. **Add the agent flow to the topic**

1. After all questions, use the **Call an action** node, and select the flow: onboarding agent

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image57.png)

1. Map the following variables:

    - text_1: empname
    - text_2: empId
    - text_3: email
    - text_4: dept
    - text_5: doj
    - text_6: dsgn
    - text_7: mgremail

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image58.png)

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image59.png)

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image60.png)


1. Now, add a **confirmation message as a message node**

    > **Message:**
    >
    > “Thank you for providing your onboarding details. Your request has
    > been forwarded to the HR team. You will receive a confirmation email
    > upon successful completion of the onboarding process."

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image61.png)

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image62.png)

    >[!Note] This assures the user that the onboarding process has been successfully triggered.


### Task 2: Configure Conversation start topic

Optionally configure your **Conversation start** topic to redirect to employee details so it automatically starts when the user types onboarding-related phrases.

1. Go to **Topics** \> **Systems** \> select **Conversation Start** topic.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image63.png)

1. Update the message as required and close the window.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image64.png)


### Task 3: Save and test the agent

1. Click on **Save** button to save the configuration for the agent.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image65.png)

1. Click on **Test** icon on the right corner of the window and test the agent providing the phrases added to the Conversation Start topic.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image66.png)

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image67.png)

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image68.png)

1. To validate correct email and data logging, go to MOD Admin’s outlook account to check if Manger’s email is triggered.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image69.png)

1. Now go to the employee’s Outlook account to check Employee confirmation email is triggered.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image70.png)

1. Employee input logged into the Dataverse Employee Record table.

    ![](https://raw.githubusercontent.com/technofocus-pte/agntgovrncscrtyentrprsscldepth/refs/heads/main/Labguides/Lab%202%20-%20Create%20an%20agent%20that%20helps%20HR/media/image71.png)


## Summary

In this lab, you learnt how to integrate Dataverse for data storage, use agent flow, enhance agent functionality by adding knowledge source, customize conversation topics to improve user interaction. You learnt how to automate key onboarding tasks such as generating employee records and sending emails.
