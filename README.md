# ResourceExchange
ThPower Platform solution for tracking resource requests and offers.

Resource Exchange Capability\


DEPLOYMENT GUIDE

# Solution Components:

-   Dataverse
-   Power Pages
-   Power Automate
-   Model Driven Apps
-   Microsoft Teams
-   Azure Active Directory


# Installing & Configuring the Solution: 

## Deploy The Solution

1.  Check these pre-requisites first to make sure that you are ready to deploy the solution:

    a.  Do you have a Production environment in Power Apps where you can deploy the solution?  
    [Click here](https://learn.microsoft.com/en-us/power-platform/admin/environments-overview) for more information about creating a Production Environment.

    b.  Do you have permissions to manage the Production Environment?  
    If not, or your not sure, [click here](https://learn.microsoft.com/en-us/power-platform/admin/control-user-access) to find out.

    c.  Is the Enhanced Data Model enabled on the Production environment where you are deploying the solution? 
    If you're not sure, [click here](https://learn.microsoft.com/en-us/power-platform/admin/environments-overview) to find out how to check, or [here](https://learn.microsoft.com/en-us/power-pages/admin/enhanced-data-model#enable-the-enhanced-data-model-in-an-environment) to learn how to convert to the Enhanced Data Model. *Note, as of August 2023, the Enhanced Data Model is still in 'preview'. It may take approximately 10-30 minutes to enable within your environment.*

    d.  Is a Power App *per app* license applied to the Production environment where you are deploying the solution? 
    If not, follow [these instructions](https://learn.microsoft.com/en-us/power-platform/admin/about-powerapps-perapp) to add a Power App license.

    e.  Have you added the Microsoft Dataverse database to the Production Environment? 
    [Click here](https://learn.microsoft.com/en-us/power-platform/admin/create-database) to find out how to add the Dataverse database to the Production Environment.

    f.  Do you have your tenant ID handy? 
    Click [here](https://learn.microsoft.com/en-us/azure/active-directory/fundamentals/how-to-find-tenant) to find out how to access your tenant id.

***Now that we've satisfied the pre-requisites, we're ready to move on!***

2.  Download the Solution on this Repo: [MS ResourceExchange.zip](https://github.com/GH-International/ResourceExchange/raw/main/MSResourceExchange.zip)

3.  Import solution zip file into a production-type environment in PowerApps.

![image](https://github.com/GH-International/ResourceExchange/assets/527590/50e6e833-bc1b-412e-b423-04e4d8b16141)

*Note: it may take 30-60 minutes for solution to be fully functional*

4. Once the solution is imported, click the **Publish all Customizations** link on the main menu.
   ![image](https://github.com/GH-International/ResourceExchange/assets/527590/e91fde0a-06ac-4d6b-8e64-59f1e6db74ab)

 
## Configure the Solution

1.  **Rename the Power Pages Site:**

Once you deploy the solution, the Site will initially be named 'demo resource exchange'. We recommend you rename the site to something more relevant to your organization or event.

![image](https://github.com/GH-International/ResourceExchange/assets/527590/ee979761-12d2-43b0-8679-b458115ca83a)


a.  Navigate to the Power Pages Home ([https://make.powerpages.microsoft.com)](https://make.powerpages.microsoft.com) and ensure that your Production environment is selected. Go to Inactive Sites and select Reactivate.

![image](https://github.com/GH-International/ResourceExchange/assets/527590/9aa68285-7d4a-4d0d-990b-c89fd3a6426c)


b.  You will be prompted to update the website name and address. Rename the website name and address and click 'Done'.

![image](https://github.com/GH-International/ResourceExchange/assets/527590/42976eb6-ab03-4cfc-a6f5-21c523f4ee3a)


2.  **Update references to the old site and domain name in the Power Pages settings.**

    a.  Go to Power Pages Management and select Websites from the menu on the left navigation panel.

![image](https://github.com/GH-International/ResourceExchange/assets/527590/c638011c-e5ae-4376-8db0-54da876cb782)


b.  Change the **Primary Domain Name prefix** to the desired website URL that you defined in step 1.B.

![image](https://github.com/GH-International/ResourceExchange/assets/527590/f3fa4601-5889-4cb4-baf5-dd7107d61723)


c.  Click on the Site Settings section on the left navigation panel, update the **Authentication/Registration/LoginButtonAuthenticationType** by updating the existing string that follows the trailing backslash with your tenant ID.
    
![image](https://github.com/GH-International/ResourceExchange/assets/527590/83692327-c47c-46bb-96c1-36f01d6f0633)

d.  Update the **HTTP/X-Frame Options**, change the prefix in the 'allow-from' value to your domain name from step 1-B:

![image](https://github.com/GH-International/ResourceExchange/assets/527590/f595990b-4fb6-4caf-87f7-d99cc3ef222d)


3.  **Restart the Site and Go Live!**

    a.  Go to Portal Platform admin center and select **Restart Site.**

![image](https://github.com/GH-International/ResourceExchange/assets/527590/b1e0fadb-bebb-4844-9258-43b571927595)


a.  Select the **Convert to Production** button.

![image](https://github.com/GH-International/ResourceExchange/assets/527590/401cfc88-776f-41bf-9b7e-90f6a3a1c60d)

![image](https://github.com/GH-International/ResourceExchange/assets/527590/25f0322a-91c6-4924-870d-707a2ab0829a)


4.  **Update Power Automate Flows**

    a.  Navigate to the **Cloud flows** section of the Solution and select flow named **When Resource Committed -\> Post Message in Teams.**


![image](https://github.com/GH-International/ResourceExchange/assets/527590/75cd88b1-961e-4b3c-9aec-65557a54b5ab)


b.  Select **Edit \> Edit with Designer**

c.  Select the action named **Post message in a chat or Channel**

d.  Change the **Team** and **Channel names to desired locations** in your Microsoft Teams environment where you want the updates posted.

![image](https://github.com/GH-International/ResourceExchange/assets/527590/3355da79-0b3b-48fe-b93c-ec717f7e8b2d)


# Updating the Solution

1.  When applying an update to the Resource Exchange Solution from Github, download the updated solution file and import the solution into the same Production environment.

2.  Select 'Update' for the Solution Action in the Advanced settings.

![image](https://github.com/GH-International/ResourceExchange/assets/527590/b70452cb-a17c-4604-a6bd-3002a63ebe12)
