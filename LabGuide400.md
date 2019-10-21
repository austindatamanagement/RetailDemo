# Getting Started with Oracle Analytics Cloud (OAC)

![](images/300/Picture300-lab.png)  
Updated: October 10, 2019

## Introduction

This lab walks you through the steps to provision an Oracle Analytics Cloud (OAC) instance and connect it to your Autonomous Data Warehouse (ADW) instance.


**_To log issues_**, click here to go to the [github oracle](https://github.com/oracle/learning-library/issues/new) repository issue submission form.

## Objectives
-   Learn how to provision a new Oracle Analytics Cloud Instance
-   Learn how to connect the OAC instance to your to the ADW

## Required Artifacts
-   The following lab requires an Oracle Public Cloud account. You may use your own cloud account, a cloud account that you obtained through a trial, or a training account whose details were given to you by an Oracle instructor.



# Provision Oracle Analytics Cloud (OAC) and Connect to Autonomous Data Warehouse (ADW)

## Part 1. Create an OAC Instance
In this section you will create an OAC instance.


### **STEP 1: Create an OAC Instance**

-   Sign in to cloud.oracle.com with your account credentials as done in the previous labs.

-   Click on the **Hamburger menu** icon.

-   Scroll down to the **More Oracle Cloud Services** section, hover over **Platform Services** and then click on **Analytics**. 

-   Click on **Create Instance**.

-   Provide all the required information (fields specified by \*). For the **Instance Name**, input **OACRD**. For the **Region**, select from the dropdown box the same region as your ADW instance. For the **Number of OCPUs**, select from the dropdown box **2**.

-   Then click on **Next**.

![](./images/300/Picture300-24.png)

-   After validating your configuration, click on **Create**.

![](./images/300/Picture300-25.png)

-   It will take a few minutes until your instance is fully provisioned and ready to use. Note the Status and the sign which indicate that the service is being creating. Wait until this process is fully completed.

![](./images/300/OACprovision.png)

-   After a few minutes refresh your page and you will see the status and the sign are disappeared. Now your OAC instance is ready. In order to access your instance, click on the hamburger icon on the right side of your instance.

![](./images/300/expand.png)

-   Now click on **Oracle Analytics Cloud URL** which redirects you to a new page. Save this web page link for future use.

![](./images/300/OACURL.png)


-   Welcome to the Oracle Analytic Cloud! Enjoy exploring it!

![](./images/300/Picture300-29.png)




## Part 2. Connect OAC to ADW

### **STEP 1: Connect OAC to ADW**

-   In the Oracle Analytics Cloud Homepage, click on the **Create** button on the top-right and then click on **Connection** in the popped menu.

![](./images/300/Picture300-31.png)

-   Select the **Oracle Autonomous Data Warehouse Cloud** from the existing connection types.

![](./images/300/Picture300-32.png)

-   Complete all the required fields in the wizard as described in the table below and Save the connection. Note that you need the ADW instance **Wallet** file in order to be able to complete these fields (this step is similar to connecting  SQL Developer to the ADW instance). Please refer to previous labs for a refresher on how to access a Wallet file if needed.

-   You should fill the following connection fields, then click **Save**:

-   **Connection Name:** Type a name for this connection. For this lab, use **ADWRETAIL**.

-   **Client Credentials:** Click on **‘Select’** and select the zipped **Wallet** file (The **cwallet.sso** file will be automatically extracted from the **Wallet** file)

-   **Username:** Admin (the username you created during the ADW provisioning).

-   **Password:** The password you specified during the provisioning of your ADW instance.

-   **Service Name:** Select your database name and desired service level (low, medium, high) from the drop down list. For this lab, select your instance service named **ADWRETAIL_high**.

![](images/300/Picture300-33-updated.png)

-   You can now see your connection listed under the Connections tab in the Data page.

![](./images/300/Picture300-34.png)



## Part 3. Import Datasets from ADW to OAC

### **STEP 1: Import the Training Datasets for the ML Model to OAC**

-   In the Oracle Analytics Cloud Homepage, click on the **Create** button on the top-right and then click on **Data Set** in the popped menu.

![](./images/300/Picture300-41.png)

-   Select the connection that you have created in previous step.

![](./images/300/Picture300-42.png)

-   Select the **DEVELOPER** user from the list of users to import the datasets prepared in SQL Developer.

![](./images/300/Picture300-43.png)


Now we should import the **OOW_DEMO_STORES**, **OOW_DEMO_ITEMS**, and **OOW_DEMO_SALES_HISTORY** tables prepared in the SQL Developer to our OAC instance. We need the **sdsdsdsd** table for creating the graphs and the **sdsdsdsd** table for training the ML model in OAC. In the next steps, we show you how to import the **OOW_DEMO_STORES** table. You can repeat the same steps to import the **sdfsdfsdfsdfsdf** table.


-   Select the desired table (**OOW_DEMO_STORES**) from the list.

![](./images/300/Picture300-44.png)

-   Add all columns to your selection by clicking on **Add All**. The auto-generated name for the new table will work fine. Finish by clicking on **Add**. 

![](./images/300/Picture300-46.png)

-   When the data set is loaded, change the **sdsddsd** column from **Measure** type to **Attribute** type. In order to do so, click on the # sign next to the column name and select **Attribute** from the drop-down menu.

-   Do this for the following columns: **sdfsdfsdsd**, **sdsdsds**.

![](./images/300/Picture300-47.png)

-    Then click on **Apply Script**.

![](./images/300/Picture300-48.png)

-   You are done with adding the first table. Repeat the above import table steps for the other tables mentioned above.

-   After importing all tables, you can see them under the **Data Set** tab in the **Data** section.

![](./images/300/Picture300-45.png)

## Part 4. Create a Data Flow

### **STEP 1: Add the datasets**

-    


### **STEP 2: Select, Rename, Add Columns to a Master Table**

-   

## Great Work - All Done with Lab 400!
**You are ready to move on to the next lab. You may now close this tab.**
