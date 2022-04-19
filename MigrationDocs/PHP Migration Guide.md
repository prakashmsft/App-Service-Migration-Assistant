# **How to Migrate a PHP Web App Using the App Service Migration Assistant Tool**

## **Overview**

In this scenario you will use the **App Service Migration Assistant**
tool to migrate your PHP application to Azure App Service.

## **Pre-Requisites**

-   An active Azure Subscription.

-   Deploy a PHP application to Internet Information Services (IIS) on your local machine.

    ![A PHP application running on IIS on Local Machine](./media010/image1.png)

## **Migrate Using the App Service Migration Assistant Tool**

1.  Navigate to the below URL to begin download the Migration Assistant tool

    a.  <https://appmigration.microsoft.com/>

    ![Download the Migration Assistant tool](./media010/image2.png)

2.  Click the **Download** button on the right.

3.  Click the **Download** link and accept terms to begin downloading the tool.

4.  Note: Once the download completes, run the **MSI installer** (Note: Installation will only succeed for the system administrator account)

5.  Once the installation completes the tool can be launched from the desktop shortcut "AppServiceMigrationAssistant".

6.  The tool should automatically detect the website and display below.

    ![Tool displays phptestsite](./media010/image3.PNG)

7.  Select the site you wish to migrate and click **Next**.

8.  This will return the results of the pre-migration readiness checks.

9.  Errors need to be resolved prior to migration. Warnings indicate
    that while the migration can proceed, but there may be additional configuration steps required outside of the App Service Migration Assistant Tool. For more information see [Azure App Service Migration Readiness Checks.](https://github.com/Azure/App-Service-Migration-Assistant/wiki/Readiness-Checks)

    ![Assessment report for phptest site](./media010/image4.png)

10. Click **Next** to proceed.

11. You will now be at the **Login to Azure** page.

    ![Azure log in screen](./media010/image5.PNG)

12. Click **Copy Code & Open Browser** next to the device code. Then click **Next**. This will launch the default browser window. Once this is completed, you should see a page like the one below.

    ![Screen to paste code](./media010/image6.png)

13. Press the **Ctrl-V** key to paste the code into the field. Once the code is entered, click **Next** to continue. Note: This code expires after 10 minutes. If the code is not accepted proceed back to the assessment phase, then click next to generate a new code.

14. You will be prompted to login with your Azure account. Once you have logged in, you should see a success message.

    ![Azure App Service Migration Assistant screen](./media010/image7.png)

15. You may now close the browser and proceed back to the migration assistant tool.

16. You will now need to enter a device code for your tenant. The steps are identical to the previous step. Once the second login sign in is completed, proceed back to the tool. The tool will have advanced to the Azure Options page.

17. Fill in the options below.

    a.  Subscription.

    b.  Resource Group.

    c.  Destination Site Name.

    d.  Region.

    ![Screen to fill in above mentioned information](./media010/image8.PNG)

18. The last task on this page is to configure the database. You will need to choose between setting up a hybrid connection to your on-premises database or skipping the database setup for now. We are choosing to **skip database setup** during this time because a simple PHP website doesn't contain any database.

19. The tool will detect any connection settings from the web.config for the database if your web application has it. Click **Migrate** to proceed.

20. You will now be in the Migration Progress screen. Note this may take some time depending on the size of your site and other factors.

    ![Migration progress screen](./media010/image9.PNG)

21. Once the migration completes, the App Service Migration Assistant tool should report the migration results "Congratulations, your site has been successfully migrated!".

    ![Congratulations, your site has been successfully migrated!](./media010/image10.PNG)

22. The migration process is completed. Click **Go to your website**. The migrated site should display.

    ![Click Go to your website](./media010/image11.png)

\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
