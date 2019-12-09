# Lab 500 - Visualizations in Oracle Analytics Cloud (OAC)

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

### **STEP 1**: Create a Project

-   From Oracle Analytics Cloud, click on the hamburger menu icon and click on **Data**. 

![](./images/500/0.png)

-   Then, find **Master_Table** and click on it's hamburger menu on the far right. From there, click on **Create Project**. This will make a new project based on the dataset.

![](./images/500/1.png)


### **STEP 2**: Create a Visualization

-   If you don't see all the columns, expand **Master_Table** on the left with the **small arrow** in order to see all the columns in the data set.

![](./images/500/2.png)

-   Select these three columns **STORE_ADDRESS**, **TRANSACTIONS**, **SALES** together from the dropdown by holding down either ctrl (Windows/Linux) or command (MacOS) depending on your operating system. Once all three are selected together, right click and select **Pick Visualization...**.

![](./images/500/3.png)

-   Then, click on the **Table Icon** to make a **Table** visualization. The visualization will appear on the right.

![](./images/500/4.png)

-   Let's clean up how it looks. In the bottom left window, expand **SALES** by clicking on the **small arrow** and then click on **Number Format** and click on **Currency**.

![](./images/500/5.png)

-   Scroll down in the same window and expand **TRANSACTIONS** by clicking on the **small arrow** and then click on **Number Format** and click on **Number**.

![](./images/500/6.png)

-   Scroll down again and change **Decimal** for **TRANSACTIONS** to be **None**.

![](./images/500/7.png)

-   Finally, drag the column **SALES** from the left to the **Color** box.

![](./images/500/8.png)

-   Congratulations! You have made a visualization in just minutes that can help provide insight into the sales and transactions of various different stores. Make sure to hit **Save** in the top right to save your project.

-   The following are some other examples of what kinds of visualizations can be done in Oracle Analytics Cloud.  In the second screen capture, you can see how the machine learning data you created in this lab can be used to make prediction visualizations to give insight into future sales.

![](./images/500/9.png)

![](./images/500/10.png)


## Great Work - All Done with Lab 500!
**Congrats! You are all done. You may now close this tab.**
