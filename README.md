# ResourceExchange
Power Platform solution for tracking resource requests and offers.

Resource Exchange Capability\


DEPLOYMENT GUIDE

# Solution Components:

-   Dataverse
-   Power Pages
-   Power Automate
-   Model Driven Apps
-   Microsoft Teams
-   Azure Active Directory

# Prerequisites:

The Resource Exchange capability has a number of prerequisites which
must be met in order to deploy the solution. These prerequisites
include:

1.  User deploying the solution must have an [account with permissions
    to manage
    environment](https://learn.microsoft.com/en-us/power-platform/admin/control-user-access).

2.  Solution must be deployed to a [Production-type
    environment](https://learn.microsoft.com/en-us/power-platform/admin/environments-overview).

3.  [Enhanced Data
    Model](https://learn.microsoft.com/en-us/power-pages/admin/enhanced-data-model)
    must enabled for the environment.

4.  [Power App *per app*
    license](https://learn.microsoft.com/en-us/power-platform/admin/about-powerapps-perapp)
    must be enabled for environment.

5.  [Microsoft Dataverse
    database](https://learn.microsoft.com/en-us/power-platform/admin/create-database)
    must be added to the production environment.

6.  Must have the [tenant
    ID](https://learn.microsoft.com/en-us/azure/active-directory/fundamentals/how-to-find-tenant)
    for the Azure tenant handy.

# Installing & Configuring the Solution: 

## Deploy The Solution

1.  Check that you're ready to deploy the solution:

    a.  Do you have a Production environment in Power Apps where you can
        deploy the solution?

    b.  Do you have permissions to manage the Production Environment?

    c.  Is the Enhanced Data Model enabled on the Production environment
        where you are deploying the solution?

    d.  Is a Power App *per app* license applied to the Production
        environment where you are deploying the solution?

    e.  Have you added the Microsoft Dataverse database to the
        Production Environment?

    f.  Do you have your tenant ID handy?

***Now that we've satisfied the pre-requisites, we're ready to move
on!***

2.  Access Solution on Github here: [shawkghi/ResourceExhange
    (github.com)](https://github.com/shawkghi/ResourceExhange)

![A screenshot of a computer Description automatically
generated](media/image1.png){width="6.5in"
height="3.9583333333333335in"}

3.  Download the solution (.zip file) from Github.

4.  Import solution zip file into a production-type environment in
    PowerApps.

![A screenshot of a computer Description automatically
generated](media/image2.png){width="6.5in"
height="3.7194444444444446in"}

*Note: it may take some time (30min-1 hour) for solution to be fully
functional*

## Configure the Solution

1.  **Rename the Power Pages Site:**

Once you deploy the solution, the Site will initially be named 'demo
resource exchange'. We recommend you rename the site to something more
relevant to your organization or event.

![A screenshot of a computer Description automatically
generated](media/image3.png){width="5.683582677165354in"
height="2.353585958005249in"}

a.  Navigate to the Power Pages Home
    ([https://make.powerpages.microsoft.com)](https://make.powerpages.microsoft.com)a)
    and ensure that your Production environment is selected. Go to
    Inactive Sites and select Reactivate.

![A screenshot of a computer Description automatically
generated](media/image4.png){width="6.5in"
height="2.2958333333333334in"}

b.  You will be prompted to update the website name and address. Rename
    the website name and address and click 'Done'.

![A screenshot of a computer Description automatically
generated](media/image5.png){width="6.5in"
height="2.5743055555555556in"}

2.  **Update references to the old site and domain name in the Power
    Pages settings.**

    a.  Go to Power Pages Management and select Websites from the menu
        on the left navigation panel.

![A screenshot of a computer Description automatically
generated](media/image6.png){width="6.5in" height="2.93125in"}

b.  Change the **Primary Domain Name prefix** to the desired website URL
    that you defined in step 1.B.

![A screenshot of a computer Description automatically
generated](media/image7.png){width="6.5in" height="3.183333333333333in"}

c.  Click on the Site Settings section on the left navigation panel,
    update the **Authentication/Registration/LoginButtonAuthentication
    Type** by updating the existing string that follows the trailing
    backslash with your tenant ID.

![A screenshot of a computer Description automatically
generated](media/image8.png){width="6.5in" height="3.11875in"}

d.  Update the **HTTP/X-Frame Options**, change the prefix in the
    'allow-from' value to your domain name from step 1-B:

![A screenshot of a computer Description automatically
generated](media/image9.png){width="6.5in"
height="3.0729166666666665in"}

3.  **Restart the Site and Go Live!**

    a.  Go to Portal Platform admin center and select **Restart Site.**

![A screenshot of a computer Description automatically
generated](media/image10.png){width="6.5in"
height="3.1055555555555556in"}

a.  Select the **Convert to Production** button.

![A screenshot of a computer Description automatically
generated](media/image11.png){width="6.5in"
height="4.079166666666667in"}

![A screenshot of a computer Description automatically
generated](media/image12.png){width="4.360713035870516in"
height="2.5991896325459316in"}

4.  **Update Power Automate Flows**

    a.  Navigate to the **Cloud flows** section of the Solution and
        select flow named **When Resource Committed -\> Post Message in
        Teams.**

**\
\
**![A screenshot of a computer Description automatically
generated](media/image13.png){width="6.5in"
height="3.7270833333333333in"}

b.  Select **Edit \> Edit with Designer**

c.  Select the action named **Post message in a chat or Channel**

d.  Change the **Team** and **Channel names to desired locations** in
    your Microsoft Teams environment where you want the updates posted.

![A screenshot of a computer Description automatically
generated](media/image14.png){width="6.5in"
height="5.516666666666667in"}

# Updating the Solution

1.  When applying an update to the Resource Exchange Solution from
    Github, download the updated solution file and import the solution
    into the same Production environment.

2.  Select 'Update' for the Solution Action in the Advanced settings.

![A screenshot of a computer Description automatically
generated](media/image15.png){width="6.5in"
height="4.915972222222222in"}
