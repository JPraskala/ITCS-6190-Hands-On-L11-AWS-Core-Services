# ITCS-6190-Hands-On-L11-AWS-Core-Services

Name: Jacob Praskala

Student ID Number: 800989838

## Explanations

### Queries 

#### Query 1
Query 1 returns the first 10 rows of the Amazon dataset.

#### Query 2
Query 2 returns the count of each product category along with the total number of orders in that specific category; this is done by grouping all results by the category column.

#### Query 3
Query 3 gets the total number of orders, total units sold, and total revenue grouped by the fulfilment column. Orders that are cancelled or pending are excluded.

#### Query 4
For a given month, query 4 returns the total number of orders and the total revenue. Orders that are cancelled or pending are excluded. 

#### Query 5
Query 5 returns the top 5 SKUs in each category ranked by the total revenue. The category, SKU, total revenue, total units sold, and rank are all output in the result table. Cancelled or pending orders, as well as orders with a quantity of 0, are excluded from the query. 

### AWS Components 

#### CloudWatch

##### Description
CloudWatch is a monitoring and management service built for developers on AWS. CloudWatch provides users with data and insights to monitor your applications, respond to performance changes, optimize resource utilization, and get a health check on the system. The component collects the data through logs, metrics, and events; a user can use CloudWatch to visualize logs, visualize metrics, and discover any insights in your application that can be used to make improvements. 

#### IAM 

##### Description
IAM (AWS Identity and Access Management) allows you to control access to AWS services and resources for your group, users, and roles. With IAM, a user can manage access through permissions, which can specify who can access the services and resources. Additionally, across multiple AWS accounts, a user can manage user access through the AWS IAM Identity Center.


#### S3

##### Description
S3 is an object storage service that offers industry-leading scalability, data availability, security, and performance. Using S3, customers can protect any amount of data for a variety of usages such as web applications. S3 has a 99.9999999% durability rate, and companies all over the world use it to store millions of data-intensive applications.


## Approaches 

### Queries 

For the queries, my approach was to use my prior SQL knowledge to solve the problems. I do have experience writing SQL queries and know advanced commands, such as the WITH statement that allows you to create a temporary query and the DENSE_RANK() function as well. If I was unsure of how to write a specific command, I used external resources such as Google to get an explanation. For example, I forgot how the DENSE_RANK() function works, and after consulting Google, I understood what to write. 

### AWS Components 

#### CloudWatch

##### Description

In this assignment, I created a crawler using AWS Glue called `handson-l11-crawler`. After creating the crawler, I ran it, which transferred the data from the Amazon CSV file into an SQL table. While the crawler was running, CloudWatch output messages through its logs, which included a timestamp and a message. From the screenshot below, it can be seen the crawler was successfully executed and a table was created.

##### Screenshot

<img width="1918" height="866" alt="log_events_screenshot" src="https://github.com/user-attachments/assets/c421efa2-f920-41d8-aa3c-922ab8067cb0" />

#### IAM

##### Description

In this assignment, I used IAM to create a new role called `HandOn-L11`. This role has three permissions enabled, which provide full access to S3 and Glue, as well as the Glue service role permission. From the screenshot below, it can be seen the role was successfully created.

##### Screenshot

<img width="1918" height="912" alt="iam_screenshot" src="https://github.com/user-attachments/assets/d1cc6128-1c14-4775-850e-be6fc5584021" />

#### S3

##### Description

In this assignment, I created a bucket in S3 called `handson-l11-itcs-6190`, which contains the raw CSV file and the CSV files produced by the queries above. From the screenshot below, it can be seen the bucket was created and is operating as expected.

##### Screenshot
<img width="1918" height="911" alt="s3_screenshot" src="https://github.com/user-attachments/assets/a5da205a-0dec-439f-900c-fd5a309eeed7" />
