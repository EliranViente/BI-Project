# BI-Project
As part of my final project in industrial engineering and management, we are trying to predict hospitalization or death without a clear reason for the elderly population in Israel. For this purpose, we use systematic data that we increased based on real data of 300 patients provided by one of the health funds in Israel.
Our goal in this project is to provide quality information and identify meaningful features from the data to give medical professionals valuable insights. Specifically, the business insight is to find the characteristic that most influence hospitalization or planned cardiac death among the elderly population in Israel.
For more information about the project objective and our KPIs, see the file titled "Project Objective".
After analyzing the data warehouse, we determined that a star schema would be the most efficient schema for our needs. This choice was based on the fact that our data has no hierarchical structure and is quite extensive. With the help of this scheme, we can classify and organize the information in a simple and efficient way.
Structure of the data warehouse:
![Alt text](<Assets/Pictures/The_Data Warehouse.png>)

Next, we performed a custom ETL process for each table in the data warehouse. You can find all the processes in the ETL folder in this project.

In addition, we performed an STTM process on a selected part of the original data. Can be found it in the STTM folder in this project.

In the end, we loaded all the tables after the ETL process and tried to get business insights from them using SQL and Window Function queries.
Here are some interesting queries we did:
![Alt text](<Assets/Pictures/Fact_Table.png>)

Calculation of the duration between each test or hospitalization that each patient had:
![Alt text](Assets/Pictures/Q1.png)

According to the result of the previous query, display the patients who were admitted and had their last routine examination more than 700 days ago.
Note: The user will most likely use this query to filter exceptions.
![Alt text](Assets/Pictures/Q2.png)
## Conclusion:
This query displays the selected filter value for not referring to a hospitalization line due to the fact that the last test line necessarily resulted in hospitalization. We note that the selection of the value is a np_hard problem that affects the data that will be presented to the client. In addition, in the ETL process, we filtered outliers for 900 days, we presented here for 700 days so that an output is shown to the user. The number of days will be subject to the customer's decision to allow him to choose the number of days he would like to filter.

The number of patients who died by age:
![Alt text](Assets/Pictures/Q3.png)
## Conclusion:
The client will be able to characterize whether more deaths occurred at a certain age than at other ages and thus analyze the data of the test results in a targeted manner.

Average length of hospitalization:
![Alt text](Assets/Pictures/Q8.png)
## Conclusion:
The average length of hospitalization is an important figure by which the customer can estimate the average cost of hospitalization for his insured customers in terms of money. This figure will support the project's goal of reducing the amount of hospitalizations in the future.


Finally, due to the fact that the data is engineered and not real, there are many gaps and duplicates that affect the displayed query outputs. For this reason and because the output obtained is partial and not reflective, we did not see fit to draw general conclusions. However, at the end of each query, state what insights and conclusions the client can draw from performing them.
We do think that when the customer enters the real data, he will be able to get a lot of important insights, for example, following query number 8, the customer can focus on the age group in which the most tests were performed and try to characterize and analyze the data and test results for the age population with the highest risk of hospitalization.

# Note:
Chronological order for reading the project:
1. The project's primary purpose are in the file: "Business intelligence project instructions 2023.pdf"
2. The purpose of the project and the definition of the indicators is in the file: "The Project Goal .pdf"
3. The data warehouse definition is in the file: "Data Warehouse definition.pdf"
4. The ETL process implementation is in the ETL folder
5. The STTM process application is in the STTM folder.
6. Analysis of the data warehouse by queries and conclusions is in the Querys folder
