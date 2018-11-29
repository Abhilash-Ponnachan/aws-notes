AWS Services Overview
=====================

### AWS Global Infrastructure
Main concepts :  
* Region - A geographical area such as North America, EMEA, APAC etc. Each region has 2 or more Avialability Zones (AZs).
* Availability Zones - An AZ is simply one or more Data Centers. We can assign our resources to an AZ. The AZs within a region are connected via low-latency network.
* Edge Locations - These are distributed services meant to cache data (CDN), nearer to the consumer as they are accessed.

As of 2017 there are around 16 regions and roughly 44 AZs and many more Edge Locations (circa 90). These numbers are constantly growing.

### Core Services :
### Compute
This set of services are the main work horse of cloud computing providing the compute workload services such as VMs, Containers, and Serverless.  
Taking each one by one we have:
1) EC2 (Elastic Compute Cloud) - These are VMs in the cloud. This is perhaps the oldest service.
2) EC2 Container Service - Containers such as Docker as a service.
3) EBS (Elastic Beanstalk) - PaaS for applications.
4) Lambda - Serverless service.
5) Lightsail - Watered down version of EC2, with just a server and RDP or SSH.
6) Batch - Batch computing in the cloud.

### Storage
These services provide data storage in various ways.
Going over the list we have:
1) S3 (Simple Storage Service) - Object based storage into logical compartments called 'buckets'.
2) EFS (Elastic File Structure) - Network file storage in the cloud (think NFS).
3) Glacier - Archival data storage, cheap storage.
4) Snowball - Phyiscal disks transported to AWS DC for large volumes rather than sending across network.
5) Storage Gateway - Virtual appliances for replication back to EC2.

### Databases
Database services in the cloud, and we have the following:
1) RDS (Relational DB Services) - MySQL, MS SQL, Aurora etc, PostgressSQL.
2) DynamoDB - Non-relational (No-SQL) database (like MongoDB).
3) Elastic Cache - Caching commonly consumed accessed data.
4) Red Shift - Data warehouse for analytical data.

### Migration
1) AWS migration Hub - Track applications as we migrate them to AWS.
2) Application Discovery Service - Tracking applications and their dependencies in our portfolio.
3) DB Migration Services - A service to migrate DB from on-prem to AWS.
4) Server Migration Services - A service to track ana manage our servers as we migrate them from on-prem to AWS.
5) Snowball - Physical storage to transport large volume of data to AWS DC. It is also calssified as a storage service.

### Networking & Content Delivery
1) VPC (Virtual Private Cloud) - Virtual network around our resources. You normally configure the network CIDR, ACLs, Route tables etc.*VPC is a fundamental part of any cloud infrastructure that it is essential to master this service*. 
2) CloudFront - CDN service that can cache media assets closer to the consumer.
3) Route53 - AWS DNS service.
4) API Gateway - Managing and exposing our APIs.
5) Direct Connect - A dedicated line from our on-prem/or corporate HQ to AWS (our VPC)

### Developer Tools
1) CodeStar - Collaboration on development project.
2) CodeCommit - AWS hosted source control, essentially a private git repository.
3) CodeBuild - Build service.
4) CodeDeploy - Push deployment to EC2 or Lambda.
5) CodePipeline - CI/CD pipeline to wire up the rest of the dev-tools services.
6) X-Ray - Debug and analyze serverless apps. Request tracing.
7) Cloud9 - IDE on the cloud via the brwoser.

### Management Tools
These are what we use to monitor and manage our cloud services
1) CloudWatch - Tracks metrics and performance related events. Part of the sys-ops tool kit.
2) CloudFormation - Infrastructure as Code serive for AWS, generally via script templates.
3) CloudTrail - Logs changes to your AWS instances. By default it is turned on and stores data only for one week. Very helpful for investigation and analysis.
4) Config - Keeps a record of your AWS configuration as snapshots.
5) OpsWork - Uses Chef & Puppet to configure the environment.
6) Service Catalog - Catalog of approved services, used mainly for compliance and governance.
7) Systems Manager - Used for managing EC2 instance, patching etc.
8) Trusted Advisor - Advise around various services, like security, utlization etc.
9) Managed Services - AWS managed services can provide managed services to manage your subscriptions.

### Media Services
These are brand new as of 2017
1) Elastic Transcode - 
2) MediaConvert - File based video transcoder.
3) MediaLive - File based video feed for broadcast.
4) MediaPackage -
5) MediaStore - Service optimized to store media.
6) MediaTailor - 

### Machine Learning
1) SageMaker - Deep learning service. More neural-network based.
2) Comprehend - Sentiment analysis.
3) DeepLens - AI aware camera, that is self contained and does not need to connect out to service.
4) Lex - NLP service used for chat and Alexa.
5) Machine Learning - More basic ML algorithms. Used by Amazon for its recommendations engine.
6) Polly - Text to speech convertor. We shall use this to convert our notes to MP3 files, and stream them.
7) Rekognition - Image recognition from images and videos!
8) Amazon Translate - Amazon's version of Google Translate.
9) Transcribe - Speech recognition and turn that into text. A good combination with Polly & Translate.

### Analytics
1) Athena - Run SQL queris against data in S3 buckets (like spreadsheet), it is serverless.
2) EMR (Elastic Map Reduce) - Big-Data solution as a service.
3) CloudSearch - 
4) EalsticSearch Service - Search services.
5) Kinesis - Stream processing service.
6) Kinesis Video Stream - More a media service. Ingest media streaming service.
7) QuickSight - AWS BI tool.
8) Data Pipeline - 
9) AWS Glue - ETL service.

### Security, Identity & Compliance
1) IAM (Identity Access Management) - Identity provider, management & authentication.
2) Cognito - Device authentication (temperory), after primary auth over IAM.
3) GuardDuty - Monitors for malicious activity on AWS account
4) Inspector - Agent on EC2 instance, to inspect for security vulnerabilities.
5) Macie - Scans S3 bucktes for PII.
6) Certificate Manager -  Manage SSL certificates for AWS instances. Can be CA.
7) CloudHSM - Hardware Security Module - dedicated h/w to store encrypted keys.
8) Directory Services - Integrating MS Active Directory services with AWS.
9) WAF (Web Application Firewall) - Like Layer7 FW - application level vulnerability protection - XSS, SQL-Injection etc.
10) Shield - It stops DDOS attacks. By default for many services like CLoudFront, LB etc.
11) Artifact - Download reference documentation on governance.

### Mobile Services
1) Mobile Hub - Management console for configuring mobile apps to mobile backend.
2) Pinpoint - Tragetted push notifications.
3) AppSync - Auto update of data between mobile and online.
4) DeviceFarm - Testing mobile apps on test devices.
5) Mobile Analytics - 

### AR & VR
1) Sumerian - AR, VR & 3D application design - still in preview.

### Application Integrations
1) Step Functions - Integrate Lambda functions
2) Amazon MQ - Similar to RabbitMQ, cloud MQ services.
3) SNS (Simple Notification Service) - Notification service.
4) SQS (Simple Queue Service) - Resilient queue service for decoupling.
5) SWF (Simple Workflow Service) - Workflow managing and orchestration service.

### Customer Engagement
1) Connect - Contact center as a service!
2) SES (Simple Email Service) - Scalable email sending sevice.

### Business Productivity
1) Alex for Business - Alexa used for IT support like use cases.
2) Chime - Video conferencing service.
3) Work Docs - Secure document storage, like Dropbox.
4) WorkMail - Amazon flavour of O365, use work email for AWS.

### Desktop & App Streaming
1) Workspaces - VDI service within AWS and streaming down to our device.
2) AppStream 2.0 -  Application running on AWS instance then streamed down to device (similar to Citrix).

### IoT
1) ioT - Suite of services for IoT
2) iOt Device Mangement - 
3) Amazon Free RTOS - Free OS for micro controllers
4) Greengrass -

### Game Development
1) GameLift - Game development for AWS cloud.

## Services for SA Associate exam ##
The services that come in the scope of the AWS Solutions Architect - Associte exam are -  
![SA-Associate-scope](AWS-SA-associate-services.png)  
Again not all services in all these are equally important. The SA associate exam is quite broad in scope.

## IAM (Identity Acess Management)

### IAM 101
Setting up users and managing their access to the AWS services.  
AWS IAM provides the following capabilities -
 - Centralised control of our AWS account
 - Shared access to our AWS account
 - Granular permissions
 - Identity federation (AD, FB, LinkedIn etc.)
 - Multifactor authentication (MFA)
 - Temperory access for users/devices & services
 - Setup password rotation policies
 - Integrates with many other AWS services
 - Supports PCI DSS complaince

#### Terms & Concepts
 - User - An end user of the service
 - Group - A collection of users under one set of permissions
 - Role - An identity with a set of permission policies that determine what actions it can perform on what resource
    - We can use roles to delegate access to users, applications or services to our AWS resources
 - Policies - A document that defines one or more permissions
    - We can attach a policy document to users, groups or roles
    - A policy can be shared by multiple identities (users or roles or groups)  
    An attempt to describe the concepts and relationships visualy -![AWS-IAM-RBAC](AWS-IAM-RBAC.png)

#### IAM Lab
Once we login to the AWS console, we can find IAM service under the category __Security, Identity & Compliance__.  
__Note__ that unlike most other services, IAM is not constrained to one region. It has a _Global_ scope.  
__Root Access__ - Our Id (email) with which we created the account. It has root level permissions within our account.

Security settings for Root account
- ***MFA Configuration***  
Virtual MFA Application - Use Google Authenticator
- ***Add Other Users***  
Create user, set password, add permissions/groups/policies.
 - Create a sys admin user
   - add to 'SystemAdministrator' group
   - day to day administration
- Create a sys developer user
   - add to 'SystemAdministrator' group (for now)
   - development work
- ***Create a Role***
Create a Role for EC2 service to access S3 service.
- ***Setup Billing Alarms***
   - Setup a budget (monthly, quarterly, anually)
   - Setup an alarm when reaching a threshold of teh budget
   - Can be set for Cost, Usage, or Reservation