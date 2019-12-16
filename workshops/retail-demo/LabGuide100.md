Lab 100 - Getting Started with Autonomous Data Warehouse (ADW) and Oracle Application Express (APEX)
----------------------------------------------------------------------------


Updated: October 10, 2019

## **Introduction**

This lab walks you through the steps to get started using the Oracle Autonomous Data Warehouse (ADW) and Oracle Application Express (APEX) provided with your Autonomous Data Warehouse on Oracle Infrastructure Cloud (OCI). You will provision a new ADW instance as well as use APEX to create a workspace and user, load data, and create an app.


**_To log issues_**, click here to go to the [github oracle](https://github.com/oracle/learning-library/issues/new) repository issue submission form.

## Objectives
-   Learn how to provision a new Autonomous Data Warehouse
-   Learn how to create an APEX workspace and user
-   Learn how to load data with APEX
-   Learn how to create an app with APEX

## Required Artifacts
-   The following lab requires an Oracle Public Cloud account. You may use your own cloud account, a cloud account that you obtained through a trial, or a training account whose details were given to you by an Oracle instructor.

# Provision Autonomous Data Warehouse (ADW) and Create an App in Oracle Application Express (APEX)

In this section you will be provisioning an ADW instance using the cloud console. Then, you will use Oracle Application Express (APEX) to create a workspace with users, create an app, and load data to the app.

## Part 1. Provisioning an ADW Instance

### **STEP 1**: Sign in to Oracle Cloud

-   Go to [cloud.oracle.com](https://cloud.oracle.com), click on the **Person Icon** 

![](./images/100/Part_1_Step_1_1.png)

-   Then click on **Sign in to Cloud** to sign in with your Oracle Cloud account.

![](./images/100/Part_1_Step_1_2.png)

-   Enter your **Cloud Account Name** and click **Next**.

![](./images/100/Part_1_Step_1_5.png)

-   Enter your Oracle Cloud **username** and **password**, and click **Sign In**.

![](./images/100/Part_1_Step_1_6.png)

### **STEP 2**: Create an ADW Instance

-   Once you are logged in, you are taken to the OCI Console. Click **Create a data warehouse**

![](./images/100/Part_1_Step_2_1.png)

-  This will bring up the Create Autonomous Data Warehouse screen where you will specify the configurations of the instance. Select the root compartment, or another compartment of your choice.

-  Specify a memorable display name for the instance. Also specify your database's name, use ADWRETAIL for this lab.

![](./images/100/Part_1_Step_2_2.png)

- Then, scroll down and select the CPU core count and Storage (TB) size. Here, we use 1 CPU and 1 TB of storage.

![](./images/100/Part_1_Step_2_3.png)

-  Uncheck Auto scaling for the purposes of this workshop.

-  Then, specify an ADMIN password for the instance, and a confirmation of it. Make a note of this password.

-  For this lab, we will select License Included for the license type. If your organization owns Oracle Database licenses already, you may bring those license to your cloud service.

![](./images/100/Part_1_Step_2_4.png)

-  Make sure everything is filled out correctly, then proceed to click on **Create Autonomous Data Warehouse**.

-  Your instance will begin provisioning. Once the state goes from Provisioning to Available, click on your ADW display name to see its details.

![](./images/100/Part_1_Step_2_5.png)

-  You now have created your first Autonomous Data Warehouse instance. Have a look at your instance's details here including its name, database version, CPU count and storage size.

![](./images/100/Part_1_Step_2_6.png)

## Part 2. Creating an App with APEX

### **STEP 1**: Access APEX

-   From the Autonomous Data Warehouse instance details page, click on **Service Console**.

![](./images/100/Part_2_Step_1_1.png)

-   Then, click on **Development**.

![](./images/100/Part_2_Step_1_2.png)

-   Next, continue by clicking on **Oracle APEX**.

![](./images/100/Part_2_Step_1_3.png)

-   Sign in with your ADMIN **password** for your ADW instance that you noted down earlier and click **Sign in to Administration Services**.

![](./images/100/Part_2_Step_1_4.png)

### **STEP 2**: Create a Workspace and User

-   You will now be on the Welcome page. Click **Create Workspace**.

![](./images/100/Part_2_Step_2_1.png)

-   Then, create a Database User and Workspace Name. For this workshop, use DEVELOPER for both.

-   Then, specify a password for the DEVELOPER user. Make a note of this password.

-   Click **Create Workspace** to continue.

![](./images/100/Part_2_Step_2_2.png)

### **STEP 3**: Sign in as the New User

-   After your Workspace is created, sign out of ADMIN by clicking **ADMIN**.

![](./images/100/Part_2_Step_3_1.png)

-  Finish signing out by clicking on **Sign out**.

![](./images/100/Part_2_Step_3_2.png)

-   Then, click **Return to Sign in Page** .

![](./images/100/Part_2_Step_3_3.png)

-   Sign in to the DEVELOPER Workspace as the DEVELOPER Username with the DEVELOPER password you noted earlier and click on **Sign In** afterwards.

![](./images/100/Part_2_Step_3_4.png)

### **STEP 4**: Load Data through APEX

-   Click on **SQL Workshop**.

![](./images/100/Part_2_Step_6_1.png)

-   Then click on **Utilities**.

![](./images/100/Part_2_Step_6_2.png)

-   Finally, click on **Data Workshop**.

![](./images/100/Part_2_Step_6_3.png)

-   Continue by clicking on **Load Data** which allows you to load CSV, XLSX, XML, and JSON data.

![](./images/100/Part_2_Step_6_4.png)

-   Click **Choose File** and go the **files** folder for this workshop and select **Transactions_History.xlsx** to open.

![](./images/100/Part_2_Step_6_5.png)

-   A preview will pop up where you can view some details about the data you are loading. Proceed by entering in a **Table Name**. For this lab, use **TRANSACTION_HISTORY** for the table name. The Error Table Name will be constructed automatically.  For primary keys, leave the **Identity Column** option selected.

![](./images/100/Part_2_Step_6_6.png)

-   Finish by clicking on **Load Data**.

![](./images/100/Part_2_Step_6_7.png)

-   A table creation confirmation page should show up. Continue by clicking on **View Table** to view the table that has been added to your ADW through APEX.

![](./images/100/Part_2_Step_6_9.png)

-   Repeat the above components of STEP 6 for the **US_CENSUS.csv** data file under the **Lab Files** folder for this workshop.  When loading in this table, keep the table options for **US_CENSUS.csv** as shown below.

![](./images/100/Part_2_Step_6_18.png)

-   Confirm that the two data files you loaded have been imported as tables.

![](./images/100/Part_2_Step_6_17.png)

-   Now that the data has been loaded in, we have to make a minor change to one of the columns' data type.  With the  **TRANSACTION_HISTORY** table selected, click on **Modify Column**.

![](./images/100/Part_2_Step_6_19.png)

-   We want to modify the data type for the Date of Sale column.  To do this, select **DATE_OF_SALE (DATE)** from the **Column** dropdown.  Next, select **TIMESTAMP** from the **Datatype** dropdown.  Once you have made these selections, you can click **Next**.

![](./images/100/Part_2_Step_6_20.png)

-   The next screen asks you to confirm your column modification request.  To confirm, click **Finish**.

![](./images/100/Part_2_Step_6_21.png)

You have now changed the data type for the Date of Sale column from a Date to a Timestamp.  When the data was loaded into APEX, this column was automatically configured as a Date data type, only including the calendar date of the sale.  When we switch this column to a Timestamp data type, we not only get the calendar date of the sale, but also the time of day that the same occurred. This will come into play when we run our Machine Learning models in Lab 200.


### **STEP 5**: Create an App in APEX

-   To start creating an app, click on **App Builder**.

![](./images/100/Part_2_Step_4_2.png)

-   Next, click on **Install Sample App**.

![](./images/100/Part_2_Step_4_3.png)

-   A variety of sample apps will show up. Click on **Brookstrut Sample Application** for this lab. We will use this as our template for the app.

![](./images/100/Part_2_Step_4_4.png)

-   Then, click on **Install App**.

![](./images/100/Part_2_Step_4_5.png)

-   Continue by clicking on **Next**.

![](./images/100/Part_2_Step_4_6.png)

-   Finally, click on **Install App** to create the app.

![](./images/100/Part_2_Step_4_7.png)

-   After a few moments, the application should be installed.

### **STEP 6**: Test the App

-   Let's beging to test the app. Click on **App Builder**.

-   Hover with your cursor over **Brookstrut Sample Application** and click on the **Run button**.

![](./images/100/Part_2_Step_5_1.png)

-   Sign in to the app as DEVELOPER for the username and the DEVELOPER password you noted earlier.

-   Click on **Sign In**.

![](./images/100/Part_2_Step_5_3.png)

-   You are now able to use your app that is connected to your Oracle Autonomous Data Warehouse (ADW) instance. Have a look at some of the navigation menu options. 

-   For example, click on **Stores**.

![](./images/100/Part_2_Step_5_4.png)

-   Then, click on the store **All U Can Eat** for Store Details.

![](./images/100/Part_2_Step_5_5.png)

-   Close the app from your browser when you are ready.


## Great Work - All Done with Lab 100!
**You are ready to move on to the next lab. You may now close this tab.**
