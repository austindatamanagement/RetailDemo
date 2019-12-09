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

### **STEP 1**: Access Your APEX App

-   Navigate to and click on **Oracle APEX** from the development page of your ADW instance service console.

![](./images/300/3.png)

-   Sign in as **developer** to the **developer** workspace with the appropriate browser.

![](./images/300/4.png)

### **STEP 2**: Enable Oracle Restful Data Services (ORDS)

-   Click on **SQL Workshop** and then on **RESTful Services**.

![](./images/300/5.png)

-   Then, click on **Register Schema with ORDS**.

![](./images/300/6.png)

-   A Schema attributes window will pop up. Click **Save Schema Attributes** to continue.

![](./images/300/7.png)

## Part 2. Import and Create APIs

### **STEP 1**: Import APIs

-   Click on **Import**. 

![](./images/300/8.png)

-   Click on **Choose File** and select **ORDS_REST_DEVELOPER_salesAPI_2019_10_28.sql** from the files folder for this workshop.

-   Finish by clicking on **Import**.

![](./images/300/9.png)

>    *Note: If you encounter the error **"Unable to Import. Insufficient Priveleges"** when importing your .sql file, this means that there is a problem with your schema defined in the .sql file.  To solve this issue, you can go into the .sql file and alter the schema names to reflect whatever you named your workspace/username as in Lab 100.  In your .sql file, simply change 'DEVELOPER' to your workspace/username in the lines denoted by the arrows below. Once you have executed this change, save the file, and try again to import.*

>   ![](./images/300/9b.png)

-   The APIs have now been imported. You can view them by clicking the arrow button to expand **Modules** and then **salesAPI**. The APIs interface with the data that is on the Autonomous Data Warehouse that you have provisioned and APEX serves as the front end.

![](./images/300/10.png)


### **STEP 2**: Create APIs

-   Click on **salesAPI** to show the API template list.

-   Then click on **Create Template** to construct your own custom API.

![](./images/300/11.png)

-   We will construct a regions API that showcases all the store regions. Enter **regions** into the URI Template input field.

-   Finish by clicking on **Create Template**.

![](./images/300/12.png)

-   We will now need to create a resource handler in order for the API to run a script. Click **Create Handler** to get started.

![](./images/300/13.png)

-   The API will make a GET REST call to query the data from the ADW.

-   Change the **Source Type** to **Query**.

-   Then, input **select * from OOW_DEMO_REGIONS** into the Source box.

-   Finish by clicking on **Create Handler**.

![](./images/300/14.png)

### **STEP 3**: Check and Test APIS

-   You have now imported and created various RESTful APIs with APEX. 

-   Grab the **Full URL** of the regions API you just created and paste it into your browser and press the enter button.

![](./images/300/15.png)

-   You will see all the different regions from the data in your ADW. You can now utilize this data however you want.

![](./images/300/16.png)

-   Navigate to the **stores** API and copy and paste the Full URL into your browser to see the different stores.

![](./images/300/17.png)

![](./images/300/18.png)

## Part 3. Use HTML Web Page to Consume APIs

### **STEP 1**: Copy API URLs

-   Under **salesAPI**, click on the **stores** API and copy the **Full URL** and paste it into a separate notes file(i.e. Notepad, Microsoft Word, Apple Notes, etc.) to be used later.

![](./images/300/19.png)

-   Next, click on the **prediction** API and copy the **Full URL** and paste it into that same separate notes file.  Be sure to label which URL is which so that you do not confuse them later.

![](./images/300/20.png)

### **STEP 2**: Add API URLs to Web Page Code

-   Download the **WebPage.zip** file from the **files** folder in this lab.

-   Go to your Downloads folder and unzip the .zip file.

-   Once this folder is unzipped, navigate to the Functions.js file and open it with any IDE or text editor you have available (i.e. TextEdit, Notepad, Script Editor, Visual Studio, etc.)

-   With the .js file open, notice the **DEFINE STORES API REQUEST URL** instructions and follow the steps to paste your ‘stores’ API URL, from your notes, into the **stores_api_url** variable in the code. (Note: Refer to the image below.)

-   Next, copy your ‘prediction’ API URL, from your notes, into the **prediction_api_url** variable in the code using the **DEFINE PREDICTION API REQUEST URL** instructions provided in the code. (Note: Be sure to read the instructions carefully, as they are different than the instructions for the ‘stores’ API URL.)

![](./images/300/21.png)

-   Once you have replaced the two URLs, you must resave the file. (Note: Make sure that you keep the .js file type when you save the file in your text editor. Also, be sure that when you are saving the updated file, you are replacing the original file in the **WebPage** folder.)

### **STEP 3**: Test API Calls on Web Page

-   You have now implemented your API URLs from APEX into the code for the HTML Web Page, so your APIs are ready to be consumed!

-   Navigate again to the **WebPage** folder in your downloads.

-   To open the web page, right click on the **Layout.html** file, select **Open With**, and select the web browser of your choice (Google Chrome and Safari supported).

-   When the web page opens up, you can navigate to the **Select Store:** dropdown.  When you click on the dropdown, the list of stores is populated by the response data of your ‘stores’ REST API call using the URL you provided in the code from APEX.

![](./images/300/22.png)

-   Once you select a store from the dropdown, you can click the **See Store Details** button to see the product details for the selected store.

![](./images/300/23.png)

-   The store details table is populated with the response data from the ‘products’ REST API call using the URL you provided in the code from APEX.

-   Now, you can use the dropdown to view any store’s inventory details!  Each time you select a new store and click the **See Store Details** button, a new API call is made to get the products for that specific store in order to populate the table.

## Great Work - All Done with Lab 300!
**You are ready to move on to the next lab. You may now close this tab.**
