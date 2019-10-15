# Lab 300 - Enabling Oracle Restful Data Services (ORDS) with APEX to Call and Create APIs

Updated: October 10, 2019

## Introduction

This lab walks you through the steps to enabling Oracle Restful Data Services (ORDS) with APEX in order to call and create APIs.


**_To log issues_**, click here to go to the [github oracle](https://github.com/oracle/learning-library/issues/new) repository issue submission form.

## Objectives
-   Learn how to enable Oracle Restful Data Services (ORDS) with APEX
-   Learn how to import SQL queries as APIs in APEX
-   Learn how to create a REST API using APEX


## Required Artifacts
-   The following lab requires an Oracle Public Cloud account. You may use your own cloud account, a cloud account that you obtained through a trial, or a training account whose details were given to you by an Oracle instructor.

-   Oracle SQL Developer 18.3 or later (see <a href="http://www.oracle.com/technetwork/developer-tools/sql-developer/downloads/index.html" target="\_blank">Oracle Technology Network download site</a>)
Please use SQL Developer version 18.3 or later as this version contains enhancements for key Autonomous Data Warehouse features, including using ADW behind a VPN or Firewall.


# Enabling Oracle Restful Data Services (ORDS) with APEX to Call and Create APIs

## Part 1. Enable ORDS

### **STEP 1: Access Your APEX App**

-   Navigate to and click on **Oracle APEX** from the development page of your ADW instance service console.

-   Sign in as **developer** to the **developer** workspace with the appropriate browser.


### **STEP 2: Enable Oracle Restful Data Services (ORDS)**

-   Click on **SQL Workshop** and then on **RESTful Services**.

-   Then, click on **Register Schema with ORDS**.

-   A Schema attributes window will pop up. Click **Save Schema Attributes** to continue.

## Part 2. Import and Create APIs


### **STEP 1: Import APIs**

-   Click on **Import**. 

-   Click on **Choose File** and select **ORDS_REST_DEVELOPER_salesAPI_2019_10_09.sql** from the files folder for this workshop.

-   Finish by clicking on **Import**.

-   The APIs have now been imported. You can view them by clicking the arrow button to expand **Modules** and then **salesAPI**. The APIs interface with the data that is on the Autonomous Data Warehouse that you have provisioned and APEX serves as the front end.


### **STEP 2: Create APIs**

-   Click on **salesAPI** to show the API template list.

-   Then click on **Create Template** to construct your own custom API.

-   We will construct a regions API that showcases all the store regions. Enter **regions** into the URI Template input field.

-   Finish by clicking on **Create Template**.

-   We will now need to create a resource handler in order for the API to run a script. Click **Create Handler** to get started.

-   The API will make a GET REST call to query the data from the ADW.

-   Change the **Source Type** to **Query**.

-   Then, input **select * from OOW_DEMO_REGIONS** into the Source box.

-   Finish by clicking on **Create Handler**.

### **STEP 3: Check and Test APIS**

-   You have now imported and created various RESTful APIs with APEX. 

-   Grab the **Full URL** of the regions API you just created and paste it into your browser and press the enter button.

-   You will see all the different regions from the data in your ADW. You can now utilize this data however you want.

-   Navigate to the **stores** API and copy and paste the Full URL into your browser to see the different stores.


## Great Work - All Done with Lab 300!
**You are ready to move on to the next lab. You may now close this tab.**
