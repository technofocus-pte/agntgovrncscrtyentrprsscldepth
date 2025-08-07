**Lab 3: Design a Smart Autonomous Agent for Recruitment Workflows**

**Estimated Duration**: 60 min

**Objective**: In this lab, you will learn how to automate the HR
recruiting process by building an Autonomous Copilot Agent that analyses
candidate applications, shortlists candidates based on job descriptions,
saves their details into Dataverse, and sends interview invitations to
selected candidates. You will create an agent that can perform the
following activities: 

- Analyze Candidate Details: The copilot automatically analyses
  application received by email, extracting relevant details.

- Match Job Requirements: The copilot compares the extracted candidate
  details with job descriptions. If the candidate meets the
  qualifications, they are shortlisted.

- Shortlist and Data Entry: Shortlisted candidates' details are saved
  into Dataverse, streamlining the data entry process for HR staff.

- Send Interview Invitations: For selected candidates, the copilot
  automatically sends an email with interview details, including the
  date, time, and location, eliminating the need for HR to send these
  manually.

## **Exercise 1: Create and Configure Contoso Agent**

1.  In the Copilot Studio home section from top select the **Dev One**
    environment.

> ![](./media/image1.png)

2.  On the Welcome copilot studio tab, click on the **Skip** to move
    forward.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image2.png)

3.  From left navigation bar select **Create** and then select **New
    agent** to start creating new agent.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image3.png)

4.  From top right corner click on **Skip to configure** button.

> ![](./media/image4.png)

5.  Enter **Name, Description and Instruction** of the agent as given
    below and click on **Create** button.

> **Name:** Contoso Interview Scheduler
>
> **Description:** The Contoso Interview Scheduler Agent automates
> hiring by analysing applicants' skills, filtering eligibility,
> scheduling interviews for qualified candidates, sending email
> notifications, and storing applicant data in Dataverse.
>
> **Instruction:** To create the Contoso Interview Scheduler Agent,
> start by setting up a Copilot agent and adding a form trigger to
> collect applicant information. Integrate a knowledge source with job
> descriptions for skill analysis. Next, build a Power Automate flow to
> schedule interviews for qualified applicants, send email notifications
> to the applicant, and store applicant details in a Dataverse table.
>
> ![](./media/image5.png)

6.  On the Overview page of Agent, **enable** the orchestrator for the
    agent.

> ![](./media/image6.png)

7.  On overview page of the agent, **disable** the “**Enable your agent
    to search all public websites**” option.

> ![A screenshot of a web search AI-generated content may be
> incorrect.](./media/image7.png)

8.  From the top right corner of the agent, click on
    the **Settings** button.

> ![](./media/image8.png)

9.  Then go to the **Generative AI** section, select **Yes - Responses
    will be dynamic, using available tools and knowledge as
    appropriate**.

> ![](./media/image9.png)

10. Scroll down and set content moderation as **Medium** by using
    horizontal slider and click on **Save** to save the setting.

> ![](./media/image10.png)

## **Exercise 2: Get Started with Power Apps**

### **Task 1: Set Up a Dataverse Table**

1.  Go to Power Apps home page using <https://make.powerapps.com/>. From
    the environment selector, select the **Dev One** environment.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image11.png)

2.  From the left navigation bar select **Tables.** In the tables
    section top bar click on the **+ New table** and then
    select **Create new tables**.

> ![](./media/image12.png)

3.  Select **Import an Excel file or CSV** option to create a new table.

> ![](./media/image13.png)

4.  Click on the select form device option and select **Interview
    Schedule** excel file from **Lab Files** folder.

> ![](./media/image14.png)

5.  Select **Import**.

> ![](./media/image15.png)

6.  Select the table and click on **View data** to see the table.

> **Note:** In this case, the table is named ***Job Application***. The
> name may vary with each execution. Save the table name for future
> reference.
>
> ![](./media/image16.png)

6.  Select the first row of the table and click on the **Delete rows**.

> ![](./media/image17.png)

7.  Select **Delete**.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image18.png)

8.  Go to table data, select **Skill** down arrow, select **Edit
    column**.

> ![](./media/image19.png)

9.  Set the data type as **Text** \> **Multiple line** \> **Plain
    Text**.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image20.png)

10. and click on the **Update**.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image21.png)

8.  Select **Interview Schedule** down arrow, select **Edit column**.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image22.png)

9.  Set the data type as **Single line of text**.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image23.png)

10. click on the **Update**.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image24.png)

9.  From top right side click on **Save and exit** to save the table.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image25.png)

10. Select **Save and exit**.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image26.png)

## **Exercise 3: Configure Agent Knowledge Sources and Conversation Topics**

In this exercise, you'll learn how to enhance your agent by adding
knowledge sources and customizing conversation topics. First, you'll add
knowledge sources, including a document file and a Dataverse table, to
your agent. Then, you'll customize the conversation start topic by
modifying the default message to improve user interaction. This exercise
will help you personalize the agent’s responses and integrate relevant
data for a more efficient experience.

### **Task 1: Add Knowledge Sources to the Agent**

1.  Navigate to overview section of the agent, scroll down and click on
    the **+ Add knowledge.**

> ![](./media/image27.png)

2.  Click on the **Click to browse** button and select the lab
    file **Eligibility criteria for python developer** doc file.

> ![](./media/image28.png)

3.  After selection of file click on the **Add** button to add the file.

> ![](./media/image29.png)

3.  Again, go to the **Overview** section of the agent, scroll down and
    click on **+ Add knowledge** button.

> ![](./media/image30.png)

4.  From Add knowledge window select **Dataverse** as the source.

> ![](./media/image31.png)

5.  From the top right corner search bar search for **Job Application**,
    select **Job application** Dataverse table and click on
    the **Add** Button.

> ![](./media/image32.png)

### **Task 2: Customize the Conversation Start Topic**

1.  Navigate to the **Overview** section of the agent,
    select **Topics** from top bar and then select **Conversation
    Start** topic.

> ![](./media/image33.png)

2.  Scroll down the conversation start topic, go to Message node, after
    “virtual assistant” word remove remaining message and add **“How may
    I help you?**” message.

> ![](./media/image34.png)

3.  From top right corner click on the **Save** button to save the
    topic.

> ![](./media/image35.png)

## **Exercise 4: Test the agent**

1.  Navigate to the **Overview** section of the agent and from top right
    corner click on the **Test** to start testing.

> ![](./media/image36.png)

2.  Enter the prompt **“What is eligibility criteria?”** in the section
    and then submit it. It will return given below output.

> ![](./media/image37.png)
>
> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image38.png)

3.  Enter the prompt **“Is SQL Database is required for the python
    developer position?”** in the section and then submit it. It will
    return given below output.

> ![A screenshot of a phone AI-generated content may be
> incorrect.](./media/image39.png)

![](./media/image40.png)

## **Exercise 5: Create an Interview Scheduler Flow and Integrating It with Copilot**

In this exercise, you'll create a flow to schedule interviews and
integrate it with your Copilot agent. You'll set up a series of inputs,
such as name, email, and experience, to collect applicant information.
Then, you'll configure actions to add the data to a Dataverse table,
send an interview invitation email, and save and publish the flow.
Finally, you'll integrate the flow into your Copilot agent, enabling it
to automate the interview scheduling process.

1.  Navigate the **Overview** section of the agent, scroll down and
    click on **+ Add tool.**

> ![](./media/image41.png)

2.  Scroll down and click on the **Create a new flow** to create new
    power automate flow.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image42.png)
>
> ![](./media/image43.png)

3.  Select **When an agent calls the flow** and click on the **Add an
    input.**

> ![](./media/image44.png)

4.  Select **Text** as input type.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image45.png)

5.  Rename the input as **Name**.

> ![A screenshot of a computer program AI-generated content may be
> incorrect.](./media/image46.png)

5.  With the same process make five more input as given below:

[TABLE]

> ![](./media/image47.png)

6.  Below **When an agent calls the flow**. Right click on
    the **+** Sign and select **Add an action.**

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image48.png)

7.  In **Add an action** window search for **Add a new row** and
    select **Add a new row** action from Dataverse section.

> ![A screenshot of a computer program AI-generated content may be
> incorrect.](./media/image49.png)
>
> **Note**: Some time Dataverse connection is not created automatically,
> so participant need to **sign** in with their credential,
> authentication should be **OAuth.**
>
> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image50.png)

8.  In the table name section search and select **Job
    Application** table.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image51.png)

9.  Below table name click on **Show all** and click on the particular
    field and add the parameter with the help of dynamic content
    button **(Thunder bolt)** in the field as given below:

[TABLE]

> ![](./media/image52.png)

![](./media/image53.png)

![](./media/image54.png)

10. Collapse the **Add a new row** action pane.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image55.png)

11. Below **Add a new row** action click on the **+** Sign and
    select **Add an action.**

> ![](./media/image56.png)

12. In **Add an action** section search for **Send an email office 365
    outlook** and select **Send an email** (V2) from office 365 outlook
    section.

> ![](./media/image57.png)

12. In send an email action, select **Settings** icon for the **To**
    field and then select **Use dynamic content**.

> ![](./media/image58.png)

13. Select **Email** from dynamic content.

> ![](./media/image59.png)
>
> ![](./media/image60.png)

14. Enter the given below content in the respected fields:

[TABLE]

> ![](./media/image61.png)

14. Close the **Send an email** pane.

>  
>
> ![](./media/image62.png)

15. From the top bar **Save draft** and **Publish** the flow.

> ![](./media/image63.png)

16. Select **Go back to agent**.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image64.png)

17. Select **Untitled** flow.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image65.png)

18. Name the flow as **Interview Scheduler.**

> ![](./media/image66.png)

17. Select **Inputs**.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image67.png)

18. Click on **Customize** in **Name** field.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image68.png)

19. Enter the **Description** as **Enter the name of the applicant**.

> ![](./media/image69.png)

19. Enter the description in the respected section as given below, after
    entering the description click on the **Save** button.

[TABLE]

> ![](./media/image70.png)

## **Exercise 6: Create Python Developer Application Form in Microsoft Forms**

In this exercise, you'll create a Python Developer Application Form
using Microsoft Forms. You'll sign in to Microsoft Forms, create a new
form titled "Python Developer Application Form," and add required fields
such as name, contact number, email, experience, skills, and interview
schedule. Once the form is created, you'll collect responses by
generating a URL and testing the form to ensure it works as expected.
This exercise helps you build a structured form to gather applicant
information efficiently.

1.  Navigate to Microsoft forms
    website <https://www.microsoft.com/en-gb/microsoft-365/online-surveys-polls-quizzes> and
    click on the **Sign in** button.

> ![](./media/image71.png)

2.  Enter the admin tenant id / work or school id on the field and click
    on the **Next** button.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image72.png)

3.  Enter the password in the respected field and then click on
    the **Sign in** button.

> ![A screenshot of a computer screen AI-generated content may be
> incorrect.](./media/image73.png)

4.  Select **Yes** to stay signed in Microsoft forms.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image74.png)

5.  Close the pop-up.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image75.png)

6.  From the top left click on the **New Form** to start creating new
    form.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image76.png)

6.  Add the heading "**Python Developer Application Form**". Select
    **Quick start with** and then select **Text**.to the form and create
    the following fields with their respective types. Turn
    on **Required** for all fields.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image77.png)
>
> ![](./media/image78.png)
>
> ![](./media/image79.png)

[TABLE]

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image80.png)

7.  From the top click on the **Collect responses** button
    and **Copy** the URL.

> ![](./media/image81.png)
>
> ![](./media/image82.png)

8.  Open the new window tab and paste the URL and open the form.

> ![](./media/image83.png)

## **Exercise 7: Automate Applicant Eligibility and Interview Scheduling Using Copilot and Power Automate**

In this exercise, you'll automate the process of checking applicant
eligibility and scheduling interviews using Copilot and Power Automate.
You'll set up a trigger for when a new response is submitted to the
"Python Developer Application Form," process the responses, and check
the applicant's eligibility based on their skills and experience. If
eligible, the Interview Scheduler flow will be triggered with the
applicant's details. Finally, you will test the flow to ensure the
automation is working correctly, ensuring smooth integration of
applicant data and scheduling processes.

1.  Navigate back to copilot studio overview page window, scroll down
    and click on **+ Add trigger** button.

> ![](./media/image84.png)

2.  From the top right corner search for **Form** and select **When a
    new response is submitted** trigger and then click on
    the **Next** button.

> ![](./media/image85.png)

3.  Check if green check mark is appearing for the apps, then click on
    **Next**.

> ![](./media/image86.png)

4.  In the Form Id field select **Python Developer Application
    form** and then click on the **Create trigger**.

> ![](./media/image87.png)

4.  Select **Close** on **Add trigger** wizard.

> ![](./media/image88.png)

5.  Navigate to the **Overview** page, scroll down, click on the three
    dots **(…)** on **When a new response is submitted** trigger,
    select **Edit in Power Automate button** to start editing.

> ![](./media/image89.png)

5.  Right click on **When a new response is submitted** trigger and
    select **Delete** to remove the trigger.

> ![](./media/image90.png)
>
> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image91.png)

6.  Click on Add a trigger in the canvas, on add a trigger window search
    and select **When a new response is submitted** trigger from
    Microsoft Forms.

> ![](./media/image92.png)

7.  In **the Form Id** field, select **Python Developer Application
    Form.**

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image93.png)

8.  Below When a new response is submitted trigger, click on
    the **+** sign and select **Add an action** button.

> ![](./media/image94.png)

9.  Search and select **Get response details** action from Microsoft
    Forms section.

> ![](./media/image95.png)

10. In **Form Id** field select **Python Developer Application** Form
    and in Response Id field select **Response Id** dynamic variable
    (Thunder bolt option)).

> ![](./media/image96.png)
>
> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image97.png)

11. Close the **Get response details** pane.

> ![](./media/image98.png)

12. Select **Send a prompt to the specified copilot for processing**
    action. Enter the below given message in the body/message field.

> **Note**: There is multiple dynamic content variables are selected in
> the message please replace the message content with the help of
> dynamic content thunder bolt option.
>
> Gather information from **Python Skills (Variable)** and **How many
> years of Python development experience do you have? (Variable)**.
> Check the eligibility criteria of applicant. If applicant is eligible
> for python developer, run interview scheduler flow and use
> details **Full Name (Variable), Contact Number (Variable), Email
> Address (Variable), How many years of Python development experience do
> you have? (Variable), Python Skill (Variable), Interview Schedule
> (Variable).**
>
> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image99.png)

12. Close the pane.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image100.png)

13. From top bar click on **Save draft** and then **Publish** to publish
    the flow.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image101.png)

13. Next to Save draft button click on the **Test** to test the flow.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image102.png)

14. Select the **Manually** option and then click on the **Test.**

> ![](./media/image103.png)

15. Navigate to Form URL window and enter the following details in the
    form, then click on the **Submit**.

[TABLE]

> ![](./media/image104.png)

16. After submitting the form, navigate to flow test window, test flow
    will be completed.

> ![](./media/image105.png)

19. Go to the **Overview** section and from top right corner click
    on **Publish** and again click **Publish** to publish the copilot.

> ![](./media/image106.png)
>
> ![](./media/image107.png)

## **Exercise 8: Test the agent**

In this exercise, you will test the functionality of the agent to ensure
that it correctly processes applicant information and triggers actions
like shortlisting candidates for an interview. You will connect the
agent, initiate a test, check the Job Application table for applicant
details, and verify that an email is sent to the shortlisted candidate.
Additionally, you will test the agent's response to a prompt from the HR
Manager, ensuring the agent returns the correct details of the selected
candidate and interview schedule.

1.  Navigate to the agent **Overview** page, scroll down and click on
    the **Test** button on trigger and then select **Start testing**.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image108.png)
>
> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image109.png)

5.  The application successfully executed and applicant is shortlisted
    for the interview.

> ![](./media/image110.png)

6.  Navigate to Power Apps portal using <https://make.powerapps.com/>.
    Select **Dev One** environment.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image111.png)

7.  Select **Tables** from the left pane. Select **Job Application**
    table.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image112.png)

8.  Check the applicant details on the table.

> ![](./media/image113.png)

7.  After shortlisting the candidate, an email is sent to the applicant.

> ![A screenshot of a computer screen AI-generated content may be
> incorrect.](./media/image114.png)

8.  In the test window, HR Manager enter the prompt **“show me selected
    candidate detail and interview schedule “**. It returns the details
    of the applicants.

> ![](./media/image115.png)

**Summary**: In this lab, you learnt how to configure the agent’s
orchestrator and adjusted AI knowledge settings, created a new Dataverse
table by importing an Excel or CSV file, view and manage table data,
edited columns. You also learnt how to configure knowledge sources,
create an agent flow, create a Form using Microsoft Form to get employee
details and to test the entire workflow, ensuring that form submissions,
eligibility checks, and interview invitations were triggered as
expected.
