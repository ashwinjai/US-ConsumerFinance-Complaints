 
## Project Overview:
The "US Consumer Finance Complaints Analysis" project aims to analyze and gain insights from the Consumer Financial Protection Bureau (CFPB) complaint. The Project is built using
SQL Server integration Services (SSIS)to extract, transform, and load (ETL) the data from CFPB database stored SQL Server Management Studio (SSMS). Additionally, SSIS is utilized 
to create a data integration package that automates the data extraction process and ensure the data remains up-to-date for regular analysis in PowerBI. 

## Business Process Description
:black_medium_small_square: **Identify the Issue** : refers to the crucial step of comprehensively recognizing and understanding the specific financial problem or challenge at hand. This involves a detailed examination of the circumstances surrounding the issue to gain clarity on its nature, scope, and potential impact <br>
:black_medium_small_square: **Submission of Details** : The Complainant needs submit all relevant details pertaining to your complaint, providing accurate and comprehensive information. <br>
:black_medium_small_square: **Contact the Financial Institution** : Reach out to the financial institution's customer support. <br>
:black_medium_small_square: **Filling of Complaint** : Fill out the complaint form with specific details about the issue and go to "File Complaint" in order to file the complaint. <br>
:black_medium_small_square: **Complaint Type** : The Complaint needs Choose the appropriate complaint type from the available options that align with concerns. The Complaint are categorised further into <br>
* Billing and Fees
* Loan and Mortgage Issues
* Credit Reporting
* Fraud and Identity Theft
* Customer Service and Communication
* Account Management
* Investment and Securities
* Insurance Claims
* Privacy Concerns
* Compliance and Regulatory Matters
* Accessibility Issues
* Other Financial Issues            <br>

:black_medium_small_square: **Final Submission** : The applicant required to complete the process by making the final submission of complaint, ensuring all required information is accurately provided to the financial Intermediary company. <br>
:black_medium_small_square: **Wait for Response** : Expect a solution or compensation if the complaint is valid. <br>
:black_medium_small_square: **Resolution** : Allow time for investigation and response from the institution or CFPB. <br>
:black_medium_small_square: **Escalate if Necessary** : Seek legal advice or contact regulatory authorities if dissatisfied with the resolution. <br>

![Business_Process 1](https://github.com/ashwinjai/US-ConsumerFinance-Complaints/assets/36980518/ca4eeda6-b13a-4eb1-8cf7-8c63a0c9c9ef)   <br>

## High level architecture diagram:


## Data Transformation & Preprocessing:
An SSIS Package is architected to encompass a collection of tasks that facilitate the processing and enhancement of data originating from a SQL Server database. 
The primary component, the Data Flow Task, is created to establish robust data pipelines for efficient data retrieval.In continuation, a Data Profiling Task is utilized to thoroughly assess 
the data quality and its suitability for analysis. Once the data profiling is complete, an Execute SQL Task is implemented to execute various SQL scripts. 
These scripts perform sorting, transformation, and manipulation of the data, leading to a notable improvement in its overall quality, ultimately preparing it for insightful analysis.
To conclude the data processing pipeline, the refined data is loaded back into the SQL Server database through another Data Flow Task. This well-structured sequence of tasks guarantees 
that the data undergoes a comprehensive process of processing, refinement, and preparation, rendering it well-suited for in-depth analysis and informed decision-making. <br>

![SSIS_1](https://github.com/ashwinjai/US-ConsumerFinance-Complaints/assets/36980518/d4ac9cfc-49bc-4937-b970-168a2e0419a9)

![SSIS_2](https://github.com/ashwinjai/US-ConsumerFinance-Complaints/assets/36980518/225eba4c-c466-4618-8dfc-218bab3727ad)

## Data Ingestion: 
Connect to the CFPB database in SQL Server and retrieve the US consumer finance complaints data, which includes information on the types of complaints, financial products, 
companies involved, timestamps, Issue faced and Company Response (Consumer, Public). <br>
![Powebi_connection1](https://github.com/ashwinjai/US-ConsumerFinance-Complaints/assets/36980518/25a08a31-f0b3-400b-9be4-faf1e6798930)

## Data Transformation & Preprocessing
In this phase, data cleansing and preprocessing tasks are executed to effectively handle missing values, eradicate duplicates, eliminate irrelevant columns, and restructure the data format.
Power Query within Power BI is leveraged to perform column format transformations and create a multi-table structure, designed to suit dimension and fact tables through the utilization of Merge and Append Queries. 
Additionally, an index column is introduced in all tables to establish essential relationships between them. 
Furthermore, to generate measures and conduct table calculations, certain Aggregate and Scalar DAX queries are utilized. These measures and calculations contribute to enhancing the overall quality of the data and 
prepare it for insightful data analysis and reporting. <br>

## Data Modeling
In the data modeling phase, the implementation of the Star Schema model is adopted, wherein a central facts table is designed along with multiple dimension tables. 
During this process, some dimensions are normalized while adhering to cardinality rules. To achieve this, attributes with one-to-many relationships are split, establishing hierarchies within the Power BI Data Model components. 
Consequently, the relationships between attributes in Power BI are set to be single-directional, ensuring an organized and efficient data model structure. <br>

![PowerBI_DataModel](https://github.com/ashwinjai/US-ConsumerFinance-Complaints/assets/36980518/9fa0e571-d1e8-4a19-9b95-ccab107ef608) <br>

## Power BI Dashboard

![Dashboard_Pic](https://github.com/ashwinjai/US-ConsumerFinance-Complaints/assets/36980518/26209845-2fbe-4551-ac60-4d0b60870926) <br>







![ezgif com-optimize](https://github.com/ashwinjai/US-ConsumerFinance-Complaints/assets/36980518/161fd889-3407-40c1-9706-a5b4ce4d212a) <br>






