<h1>Implement a Serverless Architecture on AWS</h2>
<h2>Scenario</h2>
I am creating an inventory tracking system. Stores from around the world will upload an inventory file to Amazon S3. My team wants to be able to view the inventory levels and send a notification when inventory levels are low.
In this lab, I will:
<ol>
  <li>I will upload an inventory file to an Amazon S3 bucket.</li>
  <li>This upload will trigger a Lambda function that will read the file and insert items into an Amazon DynamoDB table.</li>
  <li>A serverless, web-based dashboard application will use Amazon Cognito to authenticate to AWS. The application will then gain access to the DynamoDB table to display inventory levels.</li>
  <li>Another Lambda function will receive updates from the DynamoDB table. This function will send a message to an SNS topic when an inventory item is out of stock.</li>
  <li>Amazon SNS will then send you a notification through short message service (SMS) or email that requests additional inventory.</li> 
</ol>

<h2>Lab overview</h2>
Traditionally, applications run on servers. These servers can be physical (or bare metal). They can also be virtual environments that run on top of physical servers. However, you must purchase and provision all these types of servers, and you must also manage their capacity. In contrast, you can run your code on AWS Lambda without needing to pre-allocate servers. With Lambda, you only need to provide the code and define a trigger. 

The Lambda function can run when it is needed, whether it is once per week or hundreds of times per second. You only pay for what you use.
This lab demonstrates how to trigger a Lambda function when a file is uploaded to Amazon Simple Storage Service (Amazon S3). 

The file will be loaded into an Amazon DynamoDB table. The data will be available for you to view on a dashboard page that retrieves the data directly from DynamoDB. This solution does not use Amazon Elastic Compute Cloud (Amazon EC2). It is a serverless solution that automatically scales when it is used. It also incurs little cost when it is in use. When it is idle, there is practically no cost because will you only be billed for data storage.

What I Learned:

 • Implement a serverless architecture on AWS
 
 • Trigger Lambda functions from Amazon S3 and Amazon DynamoDB

• Configure Amazon Simple Notification Service (Amazon SNS) to send notifications



    
