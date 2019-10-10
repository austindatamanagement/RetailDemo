# Lab 200 - Creating an Oracle Machine Learning (OML) User, Granting OML User Privileges Using SQL Developer, and Using OML to Run a Machine Learning Model

Updated: October 10, 2019

## Introduction

This lab walks you through the steps to make an OML user and use SQL Developer as an interface to the ADW instance for granting user privileges. Then you will use OML to run a SQL script to generate machine learning models.


**_To log issues_**, click here to go to the [github oracle](https://github.com/oracle/learning-library/issues/new) repository issue submission form.

## Objectives
-   Learn how to make an OML user
-   Learn how to connect to your new Autonomous Data Warehouse using SQL developer
-   Learn how to grant user privileges using SQL developer
-   Learn how to run an OML script


## Required Artifacts
-   The following lab requires an Oracle Public Cloud account. You may use your own cloud account, a cloud account that you obtained through a trial, or a training account whose details were given to you by an Oracle instructor.

-   Oracle SQL Developer 18.3 or later (see <a href="http://www.oracle.com/technetwork/developer-tools/sql-developer/downloads/index.html" target="\_blank">Oracle Technology Network download site</a>)
Please use SQL Developer version 18.3 or later as this version contains enhancements for key Autonomous Data Warehouse features, including using ADW behind a VPN or Firewall.


# Creating an Oracle Machine Learning (OML) User, Granting OML User Privileges Using SQL Developer, and Using OML to Run a Machine Learning Model

## Part 1. Creating an OML User


### **STEP 1: Creating OML Users**

- Click the **Service Console** button on your Autonomous Data Warehouse details page.

![](images/LabGuide100-2ba02578.png)

- Click the **Administration** tab and click **Manage Oracle ML Users** to go to the OML user management page.

![](images/LabGuide100-18cd319d.png)

This will open a new tab within your browser that asks you for a username and password.

-   Enter **admin** as the username and use the password you specified when provisioning your ADW instance.

![](./images/100/Picture700-4.png)

**Note** that you do not have to go to this page using the same steps every time, you can bookmark this Oracle ML Notebook Admin URL and access it directly later.

-   Click **Create** button to create a new OML user. Note that this will also create a new database user with the same name. This newly created user will be able to use the OML notebook application. Note that you can also enter an email address to send an email confirmation to your user (*for this lab you can use your own personal email address*) when creating the user.

![](./images/100/Picture700-5.png)

-   Enter the required information for this user, name the user as **testuser**. If you supplied a valid **email address**, a welcome email should arrive within a few minutes to your Inbox. Click the **Create** button, in the top-right corner of the page, to create the user.

![](./images/100/Picture700-7.png)

-   Below is the email which each user receives welcoming them to the OML application. It includes a direct link to the OML application
for that user which they can bookmark.

![](./images/100/Picture700-8.png)

-   After you click **Create** you will see that user listed in the Users section.

![](./images/100/Picture700-10.png)

You will use this user later in this workshop.


## Part 2. Connect SQL Developer to the ADW Instance and Grant Privileges to OML Users 
In this section you will connect the SQL Developer to the ADW instance that you provisioned in Lab 100 and grant your OML user priveleges.


### **STEP 1: Download the Connection Wallet**
As ADW only accepts secure connections to the database, you need to download a wallet file containing your credentials first. The wallet can be downloaded either from the instance's details page, or from the ADW service console. In this case, we will be showing you how to download the wallet file from the instance's details page.

-   Go back to the Cloud Console and open the Instances screen. Find your database, click the action menu and select **DB Connection**.

![](./images/200/Picture200-34.jpeg)

-   Under Download a Connection Wallet, click **Download**.

![](./images/200/Picture200-15.jpg)

-   Specify a password of your choice for the wallet. You will need this password when connecting to the database via SQL Developer later, and is also used as the JKS keystore password for JDBC applications that use JKS for security. Click **Download** to download the wallet file to your client machine. Download the wallet to a location you can easily access, because we will be using it in the next step.
*Note: If you are prevented from downloading your Connection Wallet, it may be due to your browser's pop-blocker. Please disable it or create an exception for Oracle Cloud domains.*

![](./images/200/Picture200-16.jpg)

### **STEP 2: Connect to the database using SQL Developer**
Start SQL Developer and create a connection for your database using the default administrator account 'ADMIN' by following these steps.

-   Click the **New Connection** icon in the Connections toolbox on the top left of the SQL Developer homepage.

![](./images/200/snap0014653.jpg)

-   Fill in the connection details as below:

-   **Connection Name:** admin_high

-   **Username:** admin

-   **Password:** The password you specified during provisioning your instance

-   **Connection Type:** Cloud Wallet

-   **Configuration File:** Enter the full path for the wallet file you downloaded before, or click the **Browse button** to point to the location of the file.

-   **Service:** There are 3 pre-configured database services for each database. Pick **&lt;databasename&gt;_high** for this lab. For
example, if you the database you created was named adwfinance, select adwfinance_high as the service.

*Note* : SQL Developer versions prior to 18.3 ask for a **Keystore Password.** Here, you would enter the password you specified when downloading the wallet from ADW.

![](./images/200/Picture200-18.jpg)

-   Test your connection by clicking the **Test** button, if it succeeds save your connection information by clicking **Save**, then connect to your database by clicking the **Connect** button. An entry for the new connection appears under Connections.

-   If you are behind a VPN or Firewall and this Test fails, make sure you have <a href="https://www.oracle.com/technetwork/developer-tools/sql-developer/downloads/index.html" target="\_blank">SQL Developer 18.3</a> or higher. This version and above will allow you to select the "Use HTTP Proxy Host" option for a Cloud Wallet type connection. While creating your new ADW connection here, provide your proxy's Host and Port. If you are unsure where to find this, you may look at your computer's connection settings or contact your Network Administrator.


### **STEP 3: Grant Privileges to the OML User to Access Datasets**
In order to avoid running into an access error when you run the code in OML, grant all privleges to the OML user for the tables you created in the database.

-   Under your connection in the SQL Developer, right-click on **Station_Info** table, select **Privileges** and then select **Grant**.

![](./images/200/Picture200-41.png)

-   In the popped screen, select your OML user in the **Uers/Roles** field, mark **Grant ALL** option and click on **Apply**.

![](./images/200/Picture200-42.png)

-   You should see a message indicating that your action was successful. Repeat the same steps to also grant privileges on the table **Station_Status_Weather**.

![](./images/200/Picture200-43.png)


## Part 3. Use OML to Run a Machine Learning Script and Generate a Model

### **STEP 1: Import an OML script**

-

### **STEP 2: Run the OML script**

-


## Part 4. Use APEX to See the New OML Generated Tables

### **STEP 1: Access Your APEX App**

-

### **STEP 2: Access the New OML Generated Tables**

-


## Great Work - All Done with Lab 200!
**You are ready to move on to the next lab. You may now close this tab.**

