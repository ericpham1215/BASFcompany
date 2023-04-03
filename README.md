![image](https://user-images.githubusercontent.com/128433840/226496807-28288c2a-6cc9-454f-8e83-dd018306098a.png)

## Hello! This project deals with us going out to one of our local businesses and finding an issue that we could alleviate through systems design and development. We contacted BASF corporation, which is a German chemical producer that has a plant down here in Port Arthur, Texas.

## Problem Statement
BASF Corporation is a German chemical producer and is a publicly owned company. Founded in Germany on April 6, 1865 by Friedrich Engelhorn and became a successful businessman. He started out selling bottled gas to local pubs and workshop to managing BASF Corporation. With locations worldwide, our main focus is on one of their sites that is located in Port Arthur, Texas. Lane’s dad is the turnaround planner that tracks thousands of jobs contracted out to multiple companies. These jobs have many data points that need to be tracked and updated constantly to assure quality control and completion. Currently his assistant is manually entering these jobs which is a very tedious process. This process is very inefficient and error some. We believe we can develop a system that uses a system generated code that is assigned to specific jobs to streamline this process.  We believe this process will be significantly faster and more efficient.  

## Proposal
BASF Corporation in Texas is facing downtime when tracking job applicants through Excel. Instead of having one person keep track of over 3000 jobs, we decided to alleviate their problem by using a system where all jobs are saved in a database. We have a unique number/code that can bring up the desired task and track their information. The number code that will be automatically generated and assigned to a specific task. Multiple people will have access to this code including the contractors, quality assurance team, and the person in charge of tracking the jobs. Once a task of a certain job is completed, the contractor will turn in their code to the assistant who will then scan it.  Once scanned, the database will be updated. This will make the process much more efficient by tracking variables such as completion date, quality assurance, quality control, time to completion, resources needed, and who completed the job. These variables are very important data points that need to be accurate. With our new system we will be able to present who completed the task, the time, and the duration of the job. These metrics are important for documentation and for legal reasons.

## PIECES Framework
**Performance**

- Throughput - There have been many problems with tracking different jobs because of the manager to employee ratio

- Response time to load up 3000+ jobs in the excel sheet is takes up too much time.

**Information**

- The current system is inefficient at pulling up data of applicants stored in Excel.

- Current system lacks organization of data.

**Economics**

- This will not impact sales directly

- Reduce hours used to manually update database

**Control**

- Will reduce manual entry errors

- Will allow the user to access past, present, and maybe even future problems due to scheduling. 

**Efficiency**

- It takes a long time to find an applicant in Excel

- Only specific people have access to this file

**Service**

- The current system is very time consuming

B.	The system is difficult to keep track of

## System Feasibility

**Economic Feasibility**

•	The new system will be a cost-effective product that will improve productivity.

**Operational Feasibility**

•	Data of certain jobs will easily be located and organized through generated codes that are provided for each task. This system will save time while becoming more efficient than the old system.

**Technical Feasibility**

•	All users have access to the database

•	All users have a company phone or computer to access database 

**Schedule Feasibility**	

•	The new system will be up and running in less than 5 months.

## Old ERD System

![OLDERD](https://user-images.githubusercontent.com/128433840/226491688-5b9d93f5-1d94-404b-aa76-c1699374e534.PNG)

## New ERD System

![image](https://user-images.githubusercontent.com/128433840/226492087-4ba9b69d-23eb-4882-9191-8156ed1fa67a.png)

## Context DFD of the New System 

![image](https://user-images.githubusercontent.com/128433840/226492123-c81ac6e4-01c4-45c4-8f1d-c7c635258c8a.png)

## Level 0 DFD of the New System

![image](https://user-images.githubusercontent.com/128433840/226492147-a74fdf69-e60c-4db6-b6ff-fa1faf4a0972.png)

## Entry Definition Matrix 

| Data Element  | Description |
| ------------- | ------------- |
| Contractor_Street  | Contractor building number and street name  |
| Contractor_ZipCode  | Zip code to the area which the contractor resides  |
| Contractor_City    |  City in which the contractor resides       |
|     Employee_Street       | Employee building number and street name        |
|     Employee_ZipCode       | Zip code to the area which the employee resides        |
|        Employee_City    | City in which the employee resides        |
|     Job_ID          |  Identification number for the job       |
|      Contractor_ID      |     Identification number of the contractor    |
|         Contractor_Phone   |  Phone number of the contractor       |
|      Contractor_Email      |Email of the contractor         |
|      Contractor_FirstName      |  First name of the contractor       |
|      Contractor_LastName     | Last name of the contractor        |
|     Report_ID    |I dentification number for report   | 
|    Status     | Current status for the job  | 
|     Employee_ID    | Identification number for the employee  | 
|       Employee_Phone  | Phone number of the employee  | 
|      Employee_LastName   | Last name of the employee  | 
|     Employee_FirstName    |First name of the employee   | 
|     Job_City    | City where the task is located  | 
|     Job_ZipCode    | Zip code where the task is located  | 
|     Job_Street    | Street where the task is located  | 
|   Task ID      | Identification number for the task   | 
|    Start_Date     | Start date for the task  | 
|     End_Date    | End date for the task  | 
|      Task_Description   | Description for the task  | 


## Tables

|  Entity          |  Attributes      |      
| ------------- |------------ |
|   Job        | Job_ID(Data Element), Job_Location(Data Structure)    |     
| CONTRACTORS     |   Contractor_ID(Data Element), Contractor_Address(Data Structure), Contractor_Phone(Data Element), Contractor_Email(Data Element), Contractor Name(Data Structure) Job_ID(Foreign Key)(Data Element)        |     
|FEEDBACK(AS)    | Employee_ID(Foreign Key)(Data Element), Contractor_ID(Foreign Key)(Data Element)           |     
|EMPLOYEE                   | Employee_ID(Data Element), Employee Address(Data Structure), Employee_Phone(Data Element), Employee_Name(Data Structure)          |     
| Report     | Report_ID(Data Element), Status(Data Element), Employee_ID(Foreign Key)(Data Element), Contractor_ID(Foreign Key)(Data Element)           |     
|  TASK    |  Task_ID(Data Element), Task_Status(Data Element), Start_Date(Data Element), End_Date(Data Element), Task_Description(Data Element), Job_ID(Foreign Key)(Data Element), Contractor_ID(Foreign Key)(Data Element)       |  

# SQL QUERIES
### Contractors Table
````
SELECT *
FROM contractors;
````
![image](https://user-images.githubusercontent.com/128433840/226497511-bad20624-ae91-4387-b29a-7c1d832d10fa.png)
 
### Employees Table

````
SELECT *
FROM employees;
````
![image](https://user-images.githubusercontent.com/128433840/226498087-fbb8c125-893e-4f28-b283-231a5b76dcd8.png)

### Feedback Table

````
SELECT *
FROM feedback;
````
![image](https://user-images.githubusercontent.com/128433840/226498147-f627996a-dfb9-47e3-94bf-cdeaf6fa71ac.png)

### Jobs Table
````
SELECT *
FROM jobs;
````
![image](https://user-images.githubusercontent.com/128433840/226498218-9e474f36-4bea-4f50-af64-ec9d95f1b1d0.png)

### Report Table

````
SELECT *
FROM reports;
````
![image](https://user-images.githubusercontent.com/128433840/226498283-fa72fc7d-436c-48b1-9d7a-4bd598997312.png)

### Task Table
````
SELECT *
FROM task;
````
![image](https://user-images.githubusercontent.com/128433840/226498399-86c7752a-abe7-4f6c-bd1b-698384699d28.png)

### Contractor Hire Status Query

````
SELECT c.contractor_ID, c.contractor_first_name, c.contractor_last_name, f.hire_status, e.employee_id
FROM contractors c, feedback f, employees e
WHERE c.contractor_ID = f.contractor_ID and e.employee_ID = f.employee_ID
order by c.contractor_ID ASC
````
![image](https://user-images.githubusercontent.com/128433840/226498743-2e1a58a8-fbc4-4dac-8385-6687d69e2991.png)

### Contractor Job Task Query

````
SELECT c.contractor_ID, c.contractor_first_name, c.contractor_last_name, j.job_ID, t.task_description, t.task_ID
FROM contractors c, jobs j. task t
WHERE c.contractor_ID = t.contractor_ID and j.job_ID = t.job_ID
ORDER by c.contractor_ID ASC
````
![image](https://user-images.githubusercontent.com/128433840/226499190-080c9a28-6616-422b-8c8a-3c80d20ef99b.png)

### Job Status Query

````
SELECT DISTINCT j.job_ID, t.task_description, c.contractor_ID, status, start_date, end_date
FROM contractors c, task t, report r, jobs j
WHERE t.job_ID = j.job_ID
AND
t.contractor_ID = c.contractor_ID
AND 
r.contractor_ID = c.contractor_ID
ORDER by job_ID
````
![image](https://user-images.githubusercontent.com/128433840/226499493-eab3bcd2-5d1e-4d6e-861a-bfd17d57662b.png)

### Top Contractors Query

````
SELECT c.contractor?_ID, contractor_first_name, c.contractor_last_name, r.status
FROM contractors c, report r
WHERE c.contractor_ID = r.contractor_ID 
AND
r.status = 'Complete'
ORDER by c.contractor_ID ASC
````
![image](https://user-images.githubusercontent.com/128433840/226499703-cf626193-71d3-48b1-b6f5-ed438b62b630.png)
