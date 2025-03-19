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



    
