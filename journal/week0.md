# Week 0 — Billing and Architecture

In preparation for this project (deployment of CRUDUR”; a blogging application. I had to prepare my environment and I also came up with the architectural datagram during the first week (week 0) of the program
In this journal, I will highlight a few of the activities I had undertaken in preparation. 
1.	CREATE AWS ACCOUNT: 
a.	I created my aws account which provides the environment for my deployments. 
b.	Created an admin IAM user and assigned administrator role. With this IAM user, I will perform all administrative tasks on my aws account  instead of using the rood user. This is a recommended security measure on the account level
c.	Implemented multi-factor authentication for root account user and IAM user.
d.	I have also configured account alert and budget to limit over spending and then notify me when my infrastructure is reaching the set budget limit – This is a cost management approach
 ![budget](https://user-images.githubusercontent.com/104580680/221346963-79f1752a-b7e3-436f-8232-eb30dc7c3c96.JPG)


2.	Installed aws cli on windows10 machine
 ![installing aws-cli](https://user-images.githubusercontent.com/104580680/221346976-8a19a17e-5506-42fe-9d5f-220c94ea152e.JPG)

![aws-cli](https://user-images.githubusercontent.com/104580680/221346988-456424eb-dd94-4206-ad30-e07f66124238.JPG)


3.	Created Architecture diagram and conceptual for Crudur application using Lucid Chart.
 ![Architecture diagram task](https://user-images.githubusercontent.com/104580680/221346850-495caa29-805c-4a61-bdf1-ca0f128f7aee.JPG)


Conceptual diagram
 ![Coneptual](https://user-images.githubusercontent.com/104580680/221346836-5f9c232a-af02-45b2-8101-8d917e02b147.JPG)


The proposed components and services required to deploy the solutions as represented in the architecture includes the following: 
•	AMAZON VPC: Amazon virtual private cloud enables us to deploy an isolated virtual private network within the cloud to host our infrastructure for this project

•	AMAZON ELASTIC CONTAINER SERVICE:  We will also use Amazon ECS which provides us with a managed cluster for our application containers. This way, we will not have to bother about provisioning or managing scalability


•	AMAZON ROUTE 53: This amazon managed domain name system will also be deployed to help manage the secure routing of traffic user request to our application by translating our domain name to public IP address.

•	AMAZON INCOGNITO:  incognito is an authentication ans authorization service managed by amazon. It will be used in this deployment to control user authentication and access


•	AMAZON APPSYNCH: AppSync is a managed service that uses GraphQL to make it easy for applications to get exactly the data they need. So, we will use this to provide a single API for real time data publication and updates.

•	MONGODB:  MongoDb will be deployed to serves as database solution

•	AMAZON S3:  S3 bucket will be used to provide store for application metadata and other object data.
•	AWS LAMBDA:  The AWS  Lambda will be used to deploy our serverless functions within the application
•	HTTP WEBHOOK: We will also deploy the http wenhook to implement event-driven communication within the application modules
•	MOMENTO:   Memento offers a serverless cache. In this project, momento will be used build in more scalability and keep our costs down. Our DynamoDB requests will be cached using Momento Serverless Cache service.
