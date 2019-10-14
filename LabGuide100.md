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

## Part 1. Provisioning an ADW Instance

In this section you will be provisioning an ADW instance using the cloud console.


### **STEP 1: Sign in to Oracle Cloud**

-   Go to [cloud.oracle.com](https://cloud.oracle.com), click on the **Person Icon** and then on **Sign in to Cloud** to sign in with your Oracle Cloud account.

![](./images/100/Picture100-2.png)

-   Enter your **Cloud Account Name** and click **Next**.

![](./images/100/Picture100-3.jpg)

-   Enter your Oracle Cloud **username** and **password**, and click **Sign In**.

![](./images/100/Picture100-4.png)

### **STEP 2: Create an ADW Instance**

-   Once you are logged in, you are taken to the OCI Console. Click **Create a data warehouse**

![](images/LabGuide100-4797549d.png)

-  This will bring up the Create Autonomous Data Warehouse screen where you will specify the configurations of the instance. Select the root compartment, or another compartment of your choice.

![](./images/100/Picture100-26.jpg)

-  Specify a memorable display name for the instance. Also specify your database's name, use ADWRETAIL for this lab.

![](./images/100/Picture100-27.jpeg)

- Then, scroll down and select the CPU core count and Storage (TB) size. Here, we use 1 CPU and 1 TB of storage.

![](./images/100/Picture100-28.jpeg)

-  Uncheck Auto scaling for the purposes of this workshop.

![](./images/100/Picture100-28.jpeg)

-  Then, specify an ADMIN password for the instance, and a confirmation of it. Make a note of this password.

![](./images/100/Picture100-29.jpeg)

-  For this lab, we will select License Included for the license type. If your organization owns Oracle Database licenses already, you may bring those license to your cloud service.

![](./images/100/Picture100-37.JPG)

-  Make sure everything is filled out correctly, then proceed to click on **Create Autonomous Data Warehouse**.

![](./images/100/Picture100-31.jpeg)

-  Your instance will begin provisioning. Once the state goes from Provisioning to Available, click on your ADW display name to see its details.

![](./images/100/Picture100-32.jpeg)

-  You now have created your first Autonomous Data Warehouse instance. Have a look at your instance's details here including its name, database version, CPU count and storage size.

![](./images/100/Picture100-38.JPG)

## Part 2. Creating an App with APEX

In this section you will use Oracle Application Express (APEX) to create a workspace with users, create an app, and load data to the app.

### **STEP 1: Access APEX**

-   From the Autonomous Data Warehouse instance details page, click on **Service Console**.

-   Then, click on **Oracle APEX**.

-   Sign in with your ADMIN **password** for your ADW instance that you noted down earlier and click **Sign in to Administration Services**.

### **STEP 2: Create a Workspace and User**

-   You will now be on the Welcome page. Click **Create Workspace**.

-   Then, create a Database User and Workspace Name. For this workshop, use DEVELOPER for both.

-   Then, specify a password for the DEVELOPER user. Make a note of this password.

-   Click **Create Workspace** to continue.

### **STEP 3: Sign in as the New User**

-   After your Workspace is created, sign out of ADMIN by clicking **ADMIN** and then **Sign out**.

-   Then, click **Return to Sign in Page** and sign in to the DEVELOPER Workspace as the DEVELOPER Username with the DEVELOPER password you noted earlier and click on **Sign In** afterwards.

### **STEP 4: Install an App**

-   Click on **App Builder**.

-   Next, click on **Install Sample App**.

-   A variety of sample apps will show up. Click on **Brookstrut Sample Application** for this lab.

-   Then, click on **Install App**.

-   Continue by clicking on **Next**.

-   Finally, click on **Create App** to create the app.

-   The application is now installed.

### **STEP 5: Test the App**

-   Click on **App Builder**.

-   Hover with your cursor over **Brookstrut Sample Application** and click on the **Run button**.

-   Sign in to the app as DEVELOPER for the username and the DEVELOPER password you noted earlier.

-   Click on **Sign In**.

-   You are now able to use your app that is connected to your Oracle Autonomous Data Warehouse (ADW) instance. Have a look at some of the navigation menu options. 

-   For example, click on **Stores**.

-   Then, click on the store **All U Can Eat** for Store Details.

-   Close the app from your browser when you are ready.

### **STEP 6: Load Data through APEX**

-   Click on **SQL Workshop**, then **Utilities**, and then **Data Workshop**.

-   Continue by clicking on **Load Data** which allows you to load CSV, XLSX, XML, and JSON data.

-   Click **Choose File** and go the **Lab Files** folder for this workshop and select **Transactions_History.xlsx** to open.

-   A preview will pop up where you can view some details about the data you are loading. Proceed by entering in a **Table Name**. For this lab, use **TRANSACTION_HISTORY** for the table name. The Error Table Name will be constructed automatically.

-   Finish by clicking on **Load Data**.

-   A table creation confirmation page should show up. Continue by clicking on **View Table** to view the table that has been added to your ADW through APEX.

-   Repeat the above components of STEP 6 for the **US_CENSUS.csv** data file under the **Lab Files** folder for this workshop.

-   Confirm that the two data files you loaded have been imported as tables.


## Great Work - All Done with Lab 100!
**You are ready to move on to the next lab. You may now close this tab.**
