# Visualizations in Oracle Analytics Cloud (OAC)

![](images/500/Picture500-lab.png)  
Updated: October 10, 2019

## Introduction

This lab walks you through the steps on how you can use the Oracle Analytics Cloud to visualize entities from a database such as the results of the model created in OML.


**_To log issues_**, click here to go to the [github oracle](https://github.com/oracle/learning-library/issues/new) repository issue submission form.

## Objectives
-   Learn how to visualize entities from a database in Oracle Analytics Cloud such as an Oracle Machine Learning generated model.


## Required Artifacts
-   The following lab requires an Oracle Public Cloud account. You may use your own cloud account, a cloud account that you obtained through a trial, or a training account whose details were given to you by an Oracle instructor.



# Visualizations in Oracle Analytics Cloud (OAC)



## Part 1. Visualize results in OAC

### **STEP 1: Load Results of the OML Model to OAC**

-   In the Oracle Analytics Cloud Homepage, click on the **Create** button on the top-right and then click on **Data Set** in the popped menu.

![](./images/500/Picture500-31.png)

-   Select the connection that you have created in  **Lab 300**.

![](./images/500/Picture500-32.png)

-   Select the OML user created in **Lab 100** from the list of users to import the tables that contain the results of the model created and ran in OML.

![](./images/500/Picture500-33.png)


-  You should import tables **SSW_V_RES** and **SSW_P_RES** to the OAC instance. Import those tables as descirbed in **Step 4** in **Lab 300**. After completing these process, you should see four datasets in the data section.

![](./images/500/Picture500-34.png)



### **STEP 2: Add Datasets to the Project**

-  Open the **BikeSharePrediction** project that you imported to the OAC instance in **Lab 400**. Under the **Visualize** tab, click on the **+** icon next to the **Data Elements** and select **Add Data Set**.

![](./images/500/Picture500-41.png)

-   Select **SSW_P_RES**, **SSW_V_RES**, and **STATION_INFO** and click on **Add to Project**.

![](./images/500/Picture500-42.png)

-   Next, go to the Prepare tab and in the **Data Diagram** section, click on the **0** in the middle of the line between **SSW_P_RES** and **STATION_INFO** datasets (it appears when you move your mouse between the two datasets).

![](./images/500/Picture500-43.png)

-   In the popped window, click on Add Another Match and select **STATION_ID** and **STATIONID** in **STATION_INFO** and **SSW_P_RES**. Finally, click **OK**.

![](./images/500/Picture500-44.png)

-   Repeat **Step 4** to create a connection between **SSW_V_RES** and **STATION_INFO** datasets. Finally the Data Diagram should look like this:

![](./images/500/Picture500-45.png)



### **STEP 3: Create Desired Graphs**

-   Go back to the **Visualize** tab in the project, add a new Canvas by clicking on the **+** icon.

![](./images/500/Picture500-51.png)

-   Click on the triangle next to the Canvas name, select Rename and enter the desired name for the Canvas, e.g. **Validation (OML Model)**.

![](./images/500/Picture500-52.png)

-   In the newly created Canvas, create a **Combo** chart. Use the following values to set up the chart:

![](./images/500/Picture500-53.png)

-   **Values (Y-Axis):**  SSW_V_RES->Actual_Available_Bikes (bar)   and   SSW_V_RES->Predicted_Available_Bikes (line)

-   **Category (X-Axis):** SSW_V_RES->Last_Reported->Hour of Day

-    **Filters:** SSW_V_RES->Last_Reported (start: 8/28/17 – end: 8/29/17)   and   Station_Info->Station_Name (Avenue D & E 8 St)


-   Repeat the first two instructions in this step to create another Canvas- e.g. **Prediction (OML Model)**- to visualize the prediction results. Create a **Bar** chart in this canvas as below:

![](./images/500/Picture500-54.png)

-   **Values (Y-Axis):**  SSW_P_RES->Predicted_Available_Bikes (bar)

-   **Category (X-Axis):** SSW_P_RES->Last_Reported->Hour of Day

-   **Filters:** SSW_P_RES->Last_Reported (start: 8/31/17 – end: 9/1/17)   and   Station_Info->Station_Name (Avenue D & E 8 St)


## Great Work - All Done with Lab 500!
**Congrats! You are all done. You may now close this tab.**
