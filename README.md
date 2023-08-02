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

***Now that we've satisfied the pre-requisites, we're ready to move on!***

2.  Download the Solution on this Repo: [MS ResourceExchange.zip](https://github.com/GH-International/ResourceExchange/raw/main/MSResourceExchange.zip)


3.  Download the solution (.zip file) from Github.

4.  Import solution zip file into a production-type environment in
    PowerApps.

![image](https://github.com/GH-International/ResourceExchange/assets/527590/50e6e833-bc1b-412e-b423-04e4d8b16141)


*Note: it may take some time (30min-1 hour) for solution to be fully
functional*

## Configure the Solution

1.  **Rename the Power Pages Site:**

Once you deploy the solution, the Site will initially be named 'demo
resource exchange'. We recommend you rename the site to something more
relevant to your organization or event.

![image](https://github.com/GH-International/ResourceExchange/assets/527590/ee979761-12d2-43b0-8679-b458115ca83a)


a.  Navigate to the Power Pages Home
    ([https://make.powerpages.microsoft.com)](https://make.powerpages.microsoft.com)a)
    and ensure that your Production environment is selected. Go to
    Inactive Sites and select Reactivate.

![image](https://github.com/GH-International/ResourceExchange/assets/527590/9aa68285-7d4a-4d0d-990b-c89fd3a6426c)


b.  You will be prompted to update the website name and address. Rename
    the website name and address and click 'Done'.

![image](https://github.com/GH-International/ResourceExchange/assets/527590/42976eb6-ab03-4cfc-a6f5-21c523f4ee3a)


2.  **Update references to the old site and domain name in the Power
    Pages settings.**

    a.  Go to Power Pages Management and select Websites from the menu
        on the left navigation panel.

![image](https://github.com/GH-International/ResourceExchange/assets/527590/c638011c-e5ae-4376-8db0-54da876cb782)


b.  Change the **Primary Domain Name prefix** to the desired website URL
    that you defined in step 1.B.

![image](https://github.com/GH-International/ResourceExchange/assets/527590/f3fa4601-5889-4cb4-baf5-dd7107d61723)


c.  Click on the Site Settings section on the left navigation panel,
    update the **Authentication/Registration/LoginButtonAuthentication
    Type** by updating the existing string that follows the trailing
    backslash with your tenant ID.
    
![image](https://github.com/GH-International/ResourceExchange/assets/527590/83692327-c47c-46bb-96c1-36f01d6f0633)

d.  Update the **HTTP/X-Frame Options**, change the prefix in the
    'allow-from' value to your domain name from step 1-B:

![image](https://github.com/GH-International/ResourceExchange/assets/527590/f595990b-4fb6-4caf-87f7-d99cc3ef222d)


3.  **Restart the Site and Go Live!**

    a.  Go to Portal Platform admin center and select **Restart Site.**

![image](https://github.com/GH-International/ResourceExchange/assets/527590/b1e0fadb-bebb-4844-9258-43b571927595)


a.  Select the **Convert to Production** button.

![image](https://github.com/GH-International/ResourceExchange/assets/527590/401cfc88-776f-41bf-9b7e-90f6a3a1c60d)

![image](https://github.com/GH-International/ResourceExchange/assets/527590/25f0322a-91c6-4924-870d-707a2ab0829a)


4.  **Update Power Automate Flows**

    a.  Navigate to the **Cloud flows** section of the Solution and
        select flow named **When Resource Committed -\> Post Message in
        Teams.**

**\
\
![image](https://github.com/GH-International/ResourceExchange/assets/527590/75cd88b1-961e-4b3c-9aec-65557a54b5ab)


b.  Select **Edit \> Edit with Designer**

c.  Select the action named **Post message in a chat or Channel**

d.  Change the **Team** and **Channel names to desired locations** in
    your Microsoft Teams environment where you want the updates posted.

![image](https://github.com/GH-International/ResourceExchange/assets/527590/3355da79-0b3b-48fe-b93c-ec717f7e8b2d)


# Updating the Solution

1.  When applying an update to the Resource Exchange Solution from
    Github, download the updated solution file and import the solution
    into the same Production environment.

2.  Select 'Update' for the Solution Action in the Advanced settings.

![image](https://github.com/GH-International/ResourceExchange/assets/527590/b70452cb-a17c-4604-a6bd-3002a63ebe12)

