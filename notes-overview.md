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
==================================================

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
    - Key-value apir stored as JSON
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
   - Setup an alarm when reaching a threshold of the budget
   - Can be set for Cost, Usage, or Reservation

## AWS Object Storage & CDN
==================================================
### S3 101
S3 (Simple Storage Service) is one of the oldest service offerings by AWS. It essentially provides - _durable_, _secure_, _highly scalable_ object storage via simple web services interface. 
- S3 is _object storage_ - which means it stores the data logically wrapped with its metadata, and have its unique ID (_this is called an object_).   
It has a flat storage model without a hierarchical path like traditional file storage. This architecture makes it far easier to scale out and, also be more performant for large volumes. _Traditional block storage would have to be scaled up_.  
Behind the scene objects are replicated across different storage nodes, to ensure durability and availability.  
- We use S3 for storing documents, media, files etc. Whereas for system data such as OS, databases or applicatios we would use block storage.
- S3 has virtually unlimited storage.
- A single file can be upto 5TB!
- We pay by GB.
- S3 gives logical containers called "_bucket_" to store objects. Each bucket has a globally unique name with a unique URL to it (for e.g. https://s3-eu-west-1.amazonaws.com/acmebucket).
- S3 interaction is via HTTP request/response and a successful operation should result in an HTTP 200 status.
- ***Data Consistency model***  
S3 achieves HA (High Availability) by replicating data across multiple nodes, even data centers. Theis means that there has to be some agreed model of data consistency between write and read. The S3 model of data consistency is -
   - **Create Operation (new object)** - When we put a new object into an S3 bucket _(PUTS of new objects)_ we can expect a  _Read-after-Write_ consistency. What this means is that if we do a _read_ immediately after _putting_ a new object (has returned with a 200 status) we can be guaranteed to get the new object. _The replication across nodes for PUTS of new object is apprently synchronous. Therefore whichever node the read pulls from would have the object._ The sequence diagrams below depict the _read-after-write_ scenarios for new object -

   ![S3-create-new-obj-succ](S3-new-object-succ.png)

   ![S3-create-new-obj-prem](S3-new-object-prem.png)  

   - There is one caveat however, if we attempt a _read_ first (of an object that does not exist yet), then do a _write_ of the new object, and immediately follow with a _read_ of the same then there is no gauarantee to get that new object.  
      This scenario is depicted in the sequence diagram below -
   ![S3-new-object-read-first](S3-new-object-read-first.png)

   - **Update & Delete Operation (existing object)** - When we update (PUTS) or delete (DELETE) an existing object we should expect _Eventual Consistency_. This means that if we do a read immediately after an update/delete we may get the previous state of the object, however eventually all nodes will have the same value and we will be able to get that latest value after some time.   
   It is obvious that until the update/delete is propagated to all nodes, a read may not result in the latest updated data. We have to be mindful of this when we deisgn with S3.

- ***Key-Value Store***  
Amazon S3 has a _key-value_ store data model for storing objects. An object is a composite of the following -
   - Key - _This is the name of the object, the key with which it is identified_
   - Value - _This is the actual data - sequence of bytes_
   - Version ID - _Used for versioning the object_
   - Metadata - _Tag additional information about your data_
   - Subresources :
      - Access Control List (ACL) - _Used for controlling accessing_
      - Torrent - _Used if we want to torrent our data_

   ![S3-Bucket-Object](S3-bucket-object.png)

- ***Quality Attributes***
   - Availibility 
      - S3 is _designed_ for **99.99%** availability
      - Amazon guarantees **99.9%** availability
   - Durability
      - Amazon guarantees **99.999999999% (11 X 9s)** durability of information stored in S3!
- ***Features***
   - **Tiered Storage**
   - **Lifecycle Managment** - Configure to manage the data over time, e.g. _Archive_ after period to Aamazon Glacier.
   - **Versioning**
   - **Encryption**
   - **Access via ACL & Bucket Policies** - Bucket Policies are at _bucket_ level and ACL at _object_ level.

- ***S3 - Storage Tiers/Classes***
   - **S3 Standard** - 99.99% Availability & 11x9s Durability. Most commonly used!
   - **S3 IA** - Infrequently accessed data, but still requires _quick access_ when needed. Lower fee than S3-Standard but charges retrieval fee.
   - **S3 One Zone IA** - Infrequently accessed and stored only in one AZ, hence less durability. It is cheaper.
   - **Glacier** - Used only for archival data, and is the cheapest option. Glacier has 3 flavours -
      - Expedited - a few minutes to restore
      - Standard - 3 to 5 hours for restore
      - Bulk - 5 to 12 hours for restore

- ***S3 Pricing***
With S3 we can get charged for -
   - Storage
   - Requests
   - Storage Management Pricing - tags/metadata
   - Data Transfer Pricing
   - Transfer Acceleration - faster download/upload using _CloudFront_ (AWS CDN)  

_Note: Try to stick to region N.Virginia as that is where AWS first rolls out its new features.This way we can ensure we are always on the latest stack. Though some services are 'global' (region agnostic) in scope such as IAM._

### S3 Lab
- ***Create S3 Bucket***  
   - Creating an S3 bucket is quite straight forward from the console UI. The significant thing here is that the bucket-name should be unique (as S3 objects have universal namespace). _Generally people use their organization domain name as a prefix._  
   - **Default Access**
   - AWS takes a restrictive approach to ensure security. All newly created S3 buckets are 'private' (not for public access). All objects added to the bucket are also 'private' by default.  
   It has to be explicitly made public by going to _Permissions_ -> _Public Access Settings_ -> _Edit_.  
   After making the bucket public, the object has to be made public similarly for access.
- ***Bucket Properties***  
   An Amazon S3 bucket has various properties to manage it:
   - **Versioning** - Keep multiple versions of the same object in the bucket and mange those versions.
   - **Default Encryption** - Automatically encrypt objects when they are stored in S3.
   - **Object Lock** - Prevent object from being deleted.
   - **Tags** - Tag with metadata, use for associating with cost centers etc.
   - **Transfer Acceleration** - Enable quicker network access using edge CDN.
   - **Events** - Receive notifications when specific events occur on your bucket.
   - **Server Access Logging** - Setup access logs to view details of access requests.
   - **Object Level Logging** - Record object level API activity using _CouldTrail_ data events. This incurs extra cost.
   - **Static Web Hosting** - Host a static web site that does not require any server side web technologies. I.e. just serve files.
   - **Requestor Pay** - Option for the requestor to pay base don access, instead of the bucket owner.  
- ***Bucket Permissions***  
   Manage permissions on the bucket:
   - **Public Access**
   - **ACL**
   - **Object Policies**
   - **CORS (Cross Origin Resource Sharing)**  
- ***Bucket Management***
   Features to manage the lifetime and usage of a bucket:
   - **Lifecycle**
   - **Replication**
   - **Storage Analyitics**
   - **Metrics**
   - **Object Inventory**  

- ***Version Control***  
We can enable _Versioning_ to track and access different versions of the same object.
   - Once we enable versioning for a bucket it cannot be _disabled_, it can only be _suspended_. 
   - Once enabled the bucket keeps track of each version of the object that we upload.
   - Note that object permission is applied at the version level, which means if an object is public and we upload a new version, then the latter will not automatically be public. We have to explicitly make the new version public.
   - The URI for accessing a specific version of the object uses a query parameter _versionId_ -  
   e.g.-> https://s3.amazonaws.com/my-unique-bucket/test-1.txt?versionId=V67j9XSjHYM2Y2NBNAxqLgAOU7PN6akt  
   - Deleting an object does not actually delete it, it just adds an extra version entry for a _delete marker_. We can still see all the versions if we click _Version_ -> _Show_
   - We can restore the object by undoing this marker (simply delete that marker entry)!
   - In order to compeletly remove an object we would have to delete all versions of the object.
   - Versioning can be integrated with _Lifecycle Rules_.
   - Versioning MFA Delete capability can be used to provide additional layer of security.  
- ***Cross-Region Replication (CRR)***  
We can setup _Replication_ to synch up buckets in different regions.
   - CRR can only be setup between buckets in different regions.
   - For replication the _Versioning_ has to be enabled on the target bucket.
   - We can replicate the entire contents of the bucket or selected items based on _Tags_ or _Prefixes_.
   - The target bucket for replication can belong to a different accout, and even the ownership of the target bucket can be delegated.
   - Replication requires an IAM role to be associated with it. This enabes access control and monitoring.
   - While setting up CRR, there is a gotcha that can catch you unawares. At the step to setup the IAM role for replication we can get an error - _"Inavlid role specified in replication configuration!"_. This happens because the user yu are logged in as is an IAM user (typically non-root users are not given IAM permissions), i.e. not the _root user_. In order for replication to create the role it requires the current user to have IAM permissions.
   - Only new and modified objects after turning on CRR will get replicated over, already existing objects will not (_this is similar to Versioining, versions are created only once we turn it on, for existing objects the versions will be null_). Existing objects have to be copied over via the CLI.
   - For CLI, install the AWS CLI and then configure it with the _Access Key Id_ and _Secret Access Key_ of the desired user account.
   ```
   $ aws configure
   > ...
   ```
   After configuring we can test it by typing in a few commands to check the version, and to list the S3 buckets associated with the configured user
   ```
   $ aws --version
   > aws-cli/1.16.77 Python/3.6.0 Windows/7 botocore/1.12.67

   $ aws s3 ls
   > ...
   ```
   - To copy the contents over from one bucket the other we use the _copy_ command from the CLI
   ```
   $ aws s3 cp --recursive s3://my-source-bucket s3://my-destination-bucket
   > ...
   ```
   Note how the source and destination buckets are specified - _'s3://\<bucket-name\>'_
   - Now we can go to the console and check and, indeed our objects are copied over from the source bucket to the destination. _Note that if we look at the 'Version Id' of an object, it is a different value in both buckets (this is only for manually copied over objects as we will see)!_
   - If we now change one of the files within the _source bucket_ and upload it, the change should get replicated across almost immediately. _Note how in this case the latest version of the modified file is automatically copied over and it has the exact same 'Version Id' value in both source and destination buckets!_
   ```
   # we can upload from the command line
   $ aws s3 cp <local-path> s3://<bucket-name>
   > ...
   ```
   - Finally _deleting_ objects (whether it is just placing a _delete marker_ or deleting a spcific _version_), does not get replicated. It is by design, a safety feature to prevent removal of objects from the source bucket, also removing them from the target (which is considered a _backup_).
   - As of end 2018 we cannot replicate to multiple S3 buckets or be daisy chained, though this might change in future.  
- ***Lifecycle Managment***  
   How to manage data over time. For example move data after some duration to the cheaper S3-IA tier, then later archive it into Glacier or even permenantly delete it. AWS provides a _Lifecycle Management_ service to configure this.
    - Configure rules to transition objects to tiered storage.
    - Expire objecst based on rules.
    - _Lifecycle_ rules can have filters based on prefixes or tags for selective objects.
    - Transition rules can be applied to _current version_ and/or _previous versions_ of the object.
    - Can be applied with or without _Versioning_ turned on.
    - Minimum transition duration is 30 days.
    - An example of a typical _Lifecycle_ rule would be -  
    ![S3-Lifecycle](S3-Lifecycle.png)  
- ***CloudFront Overview***  
   CloudFront is Amazon's own CDN (Content Delivery Netwrok). A CDN is a system of distributed webservers spread geographically and can host and deliver web content based on the location of the user.  
   Some key terminology -
   - **Origin** - The source/origin of the files that are dsitributed via the CDN. In the case of AWS the origins can be S3 buckets, EC2 instances, Elastic Load Balancers, or Route 53 (the former 2 are most common)._Note that an origin does not have to be an AWS service, it can be ay other web resource_
   - **Edge Location** - The location where the content will be _cached_. This is different from _Region/AZ_, and for AWS it is spread across the globe.
       - An edge location is not just read-only, we can write to them (like put an object in). This will then behind the scene be pushed up to the origin.
       - Objects are chaced at the edge location for a duration call TTL (Time To Live).
       - Objects will automatically expire after the TTL. We can expunge/clear the cached object but we can get chraged for that!
   - **Distribution** - The logical name given to a collection of _edge locations_.
   - **Web Distribution** - Typically used for web pages.
   - **RTMP** - RTMP stands for _Real Time Media Protocol_, used for media streaming on the internet. Though RTMP is being slowly replaced by HLS (HTTP Live Streaming) protocol.  

   - ***CloudFront Lab***  
   To solidify the concepts, let us get our hands dirty and setup a CloudFront _distribution_ and test it.   
   <u>Origin</u>  
   We shall use an S3 bucket as the _origin_. Let us create one ina region far from us. In my case I am making one in Sydney. Then I give it access permissiona and upload a big mage file. Now I use a script (Python 3) to access this and measure the time it takes to download - 
   ```python
   # skipping the initial imports and proxy code

   object_url = 'https://s3-ap-southeast-2.amazonaws.com/my-sydney-bucket/my-large-image.jpg'
  
   def access_object(url):
      rsp = requests.request("GET", url, proxies=proxies)
      return rsp

   try:
      ts = time.perf_counter_ns()
      rsp = access_object(object_url)
      tt = time.perf_counter_ns() - ts
      print('status = {0} ; size = {1}'.format(rsp.status_code, len(rsp.content)))
      print('>> time taken = {0:.2f} seconds'.format(tt/1000000000))

   except Exception as ex:
      print (ex) 
   ```
   This will give us the output - 
   ```bash
      status = 200 ; size = 294718
      >> time taken = 5.81 seconds
   ```
   It takes around 5.8 seconds to download around 29KB from my S3 bucket in Sydney!  
      <u>Distribution</u>  
   We can now setup a CDN distrtibution to cache this S3 bucket and try to acess the image through the CDN. We can do this from the console and going to _Services_ -> _Networking & Content Delivery_ -> _CloudFront_
   - For this lab, we shall create a _Web Distribution_  
   <u>There are a number of options we have to specfy in order to configure the _Distribution_</u> - 
   - **Origin domain** - We select our S3 bucket -> my-sydney-bucket
      - For non AWS services we provide the web address of the resource

   - **Origin path** - If there is a directory within our bucket that we want to get the content from then we specify that with a '/'. In this case we leave it blank

   - **Origin ID** - A unique (within the distribution) name for the origin. Note that a distribution can have multiple origins 
   - **Restrict bucket access** - Setting this will prevent direct access to the _origin_, it can only be accessed via the CDN then. This is especailly useful when we want to restrict to private access via _signed URL_ or _signed cookie_. If we select _Yes_ then we have to set a few additional properties -  
      - **Origin access identity** - This creates a new user-identity which will be used to access the _origin_ (the S3 bucket in our case) from the CDN
      - **Grant read permissions on bucket** -  Give the _origin access identity_ permission to access the _origin_ (S3 bucket). Remember to click _Yes update bucket policy_ else this would have to set manually  

   _Since we are blocking direct access to the S3 bucket, there has to be some exception role/identity that can be used by the CDN to access the bucket_
   - **Viewer protocol policy** - Specify the HTTP & HTTPS behaviour. We shall use _Redirect HTTP to HTTPS_  

   - **Time To Live (TTL)** - Specify the _minimum_, _default_ & _maximum_ TTL values in seconds. We shall leave the default values for now viz. - _default TTL = 24 hrs_ & _maximum TTL = 1 year_. In a real scenario this is an important design consideration as manually invalidating the cache can incur a cost

   - **Restrict viewer access** - When we want to conditionally restrict access to our CDN resource we do that by enabling this option and then generating a _presigned URL_ or _signed cookie_ and accessing the resource using that. For example when we want to restrict access to paid customers. We will not restrict any access 

   - **Lambda Function Association** - Link events on the _distribution_ to a _Lambda Function_. We shall leave this blank  

   - **SSL certificates** - We shall use the default _cloudfront certificate_, but we can opt for a custom SSL certificate if required. Then we can configure and manage that through the _AWS certificate manager_
   - **Supported HTTP versions** - Now _CloudFront_ has support for HTTP/2 (as well as HTTP/1.1 and older)
   - **IPv6** - Recently added support for IPv6. It is enabled by default

   - **Applying Restrictions** - We can use this to apply restrictions based on geographical locations. Either _whitelist_ or _blacklist_ the countries that can access the distribution

   _Note that there are many more options and I have ignored them in this list as it is too extensive to cover each in depth. In any case we have left them all as default values!_  

   _Also note that once we create or apply changes, the actual provisioning for the distribution can take a while (15 to 20 minutes at least)_  

   Once created we would have an _ID_ and _Domain Name_ for the _distribution_ that we can use to access the resources. For example we could get a _domain name_ such as - 
   d651a7rd02db4c.cloudfront.net  
   Then we can execute the above Python script with the modified object URL via the CloudFront domain name -
   ```python
      # use the cloudfront domain name for the resource url
      object_url = 'https://d651a7rd02db4c.cloudfront.net/my-large-image.jpg
   ```  
   Now when we execute the script, we should get the following results -
    - The first run we would get something like - 
   ```bash
      status = 200 ; size = 294718
      >> time taken = 5.52 seconds
   ```
   The first access tme is no different as it is still pulling the resource down to the nearest edge location.
    - The subsequent runs we would get something like - 
   ```bash
      status = 200 ; size = 294718
      >> time taken = 1.48 seconds
   ```
   - **Reports & Analytics** - This section provides options to view and analyze the usage of our CloudFront _distributions_

   Finally we have to remember to _disable_ and _delete_ our distribution, as we can get charged for this.  
     
- ***S3 Security & Encryption***  
   - **Securiy**  
      - **Access**  
      All newly created buckets are private. If we wish to access the objects within a bucket we have to explicitly go and make them _public_ of grant access to them.  
      There are two ways to control access to S3 buckets -
         - *Bucket Policies*  
            These are buckt-wide in scope and apply to all items within the bucket.
         - *Access Control Lists (ACLs)*  
            These are more finegrained and can control access to individual objects within a bucket.
      - **Access Log**  
      S3 buckets can be configured to log all access requests. These can be logged in the same bucket, a different bucket or even the bucket of a different account!
   - **Encryption**
   There two aspects to encrypting data, namely -
      - **Encryption in Transit**  
         This is achieved using SSL/TLS  
      - **Encryption at Rest**  
         There are 2 appraoches to encrypting data at rest, namely -  
         - **Server Side Encryption (SSE)**  
         S3 provides 3 methods for SSE -
            - *S3 Managed Keys -> SSE-S3*  
            Each object is encrypted with a unique key and that key is then further encrypted with a master key. AWS mananges all the encryption keys for us behind the scene. It uses AES 256 standard.
            - *AWS Key Managment Service -> SSE-KMS*  
            Added feature of control over the envelope key so gives an added layer of protection. It also gives an audit trail of decryption. This coes with some extra charge. 
            - *SSE with Customer Provided Keys - SSE-C*  
            In this AWS only manages the encryption/decryption, but we manage the keys.
         - **Client Side Encryption**  
         This where we encrypt the data on the client and upload it to the bucket.  

- ***AWS Storage Gateway***  
AWS Storage Gateway is a storage service that enables on-premises applications to seamlessly use AWS cloud storage.  
   - The applications connect to the cloud storage service via a gateway appliance (which can be virtual or physical device)
   - They can connect to the storage using standard storage protocols such as NFS (_Network File Storage_), SMB (_Server Message Block_), iSCSI (_SCSI over IP_)
   - The gateway connects to AWS storage services such as _S3_, _EBS_ or _Glacier_ to store _Files_, _Volumes_ or _Tapes_  
   - We can use this for things such as -  
      - Storage tiering
      - Cloud data processing
      - Backup & recovery
      - Archiving
   - The implementation provides -
      - Highly optimized data-transfer
      - Bandwidth management
      - Automated network resilience
      - Local cache for recently accessed data  

Once installed and activated with our AWS account we can configure it to use the Gateway service as required.  
The diagram below depicts this setup at a basic level -  
![AWS Storage Gateway](AWS-Storage-Gateway.png)  

There are __4 types__ of Storage Gateways -   
- **File Gateways (NFS)**  
This allows us to store _files_ directly as objcets in S3. The buckets are accessed as NFS mount point. Once written to S3 the oject can be treated and managed just as we would any S3 object.  
![File-Gateway](File-gateway.png)
- **Volume Gateways (iSCSI)**  
This provides a way to use block based storage in the cloud from on-premises applications. The gateway allows us to access the cloud storage as iSCSI volumes. Think of these as _virtual hard drives_ on the cloud!  
Data written to these volumes are asynchrnously copied as point in time EBS snapshots to the cloud. These snapshots are incremental, they contain only the changed blocks. They are also compressed to minimize storage charges.  
All _Volume Gateway_ data written to the cloud is stored in Amazon S3 as EBS snapshots, they are encrypted at rest using _SSE_. However these snapshots cannot be accessed via teh S3 API or management console!   
It is importnat to keep in mind that, _Volume Gateway_ services have on-premises storage hardware associated with them.  
_Volume Gateways_ are of two types -
   - **Stored Volumes**  
    All data written to the _Stored Volume_ is written to the on-premises storage hardware associated with that volume and then, asynchronously copied over to Amazon S3 as EBS snapshosts. They can range from 1GiB to 16TiB, and a gateway can support upto 32 volumes (for a total of 512 TiB).  With _Stored Volumes_ we keep a complete copy of the data on-premises.  
   - **Cached Volumes**  
   In the case of _Cached Volume_ the primary storage is our cloud storage. All data is written to Amazon S3 (via a staging area - upload buffer). Only recently accessed data is cached locally for low-latency access. Compared to _Stored Voulme_ this approach minimizes the need for us to scale our on-premises storage capacity, while still maintaining local cache for recently accessed data. _Cached Volume_ can range from 1GiB to 32TiB.
- **Tape Gateways (VTL)**  
This option provides a cost-effective way to archive data to the cloud. We can use existing tape-based backup infrastructure to bacukup data to _virtual tape cartridges_ that we can create on the _Tape Gateway_. Each gateway is preconfigured with media changer and tape drives. The backup applications can access these as iSCSI devices. A high level diagram dpeicting this setup is given below -  
![Tape-Gateway](Tape-gateway.png)  

- ***AWS Snowball***  
Sometimes there is a need to move large volumes of data (TiB, PiB) into AWS and trying to do that over the internet can be very time consuming and even expensive. To resolve this Amazon used to provide a service called _Import/Export Disk_. We could send in an external storage disk with our data and AWS could directly transfer the data off the disk (bypassing the internet). This is a phyiscal movement of data via disks. But this poses many challenges with customers sending in different types of disks with different connections, ensuring security etc. In order to manage this, Amazon standrdized this process with a service called _Snowball_. This uses a Amazon provided phyiscal storage appliance to store and tranfer the data.  
There are 3 types of _Snowball_ services:
   - **Snowball** - These are Petabyte-scale data tranfer solutions using phyiscal appliances into or out of AWS. This addresses challenges of tranfer-time, bandwidth-costs, and security. These are highly secure, tamper-resistant, 256-bit encrypted devices with full traceability. It is also very cost effective and can be _one fifth_ the cost of tranferring over the internet. Once data is transfered AWS errases the data from the appliance. As of early 2019 they come with 80TB storage capacity.
   - **Snowball Edge** - These are essentially _Snowball_ with 100TB of storage capacity with _onboard compute_ capability! _Snowball Edge_ comes in two flavours (as of eraly 2019) -
      - *Snowball Edge Storage Optimized* - They come in 100TB with 24vCPU best for large scale data collection and migration.
      - *Snowball Edge Compute Optimized* - They provide 52vCPu and optional GPU for high performance machine learning or data analysis use cases.
   These applainces can be clustered to form larger temperory installations. The come with specific EC2 instances and _Lambda Function_. They cacn collect, pre-process and return data. Good use-cases include IoT stream processing, or pre-processing data for analysis and migration from remote locations, which would eventually transfered to AWS.
   - **Snowmobile** - _Snowmobile_ is used for Exabyte-scale data transfer. They are essentially a mini DC on wheels - A 45 foot long ruggedized shipping container pulled by a semi-trailer truck! The service is provided accompanied by specialists who help assess, connect, transfer and scecure the data. Each _Snowmobile_ has a capacity of do 100PB.  
   It comes with 256-bit encryption, full trace of chain-of-custody. In addition it has 24/7 video surveillance, security personnel and GPS tracking.  
   It is a very cost effective way to transfer huge volumes of data securly and in less time. It can even do a complete data center migration. 
A _Snowball_ can import to or export from _S3_. If we want to use _Glacier_ we would have to do it via _S3_.

- ***S3 Transfer Acceleration***  
This is a new service that allows us to leverage _CloudFront_ to accelerate transfer of data to and from S3.  
When we setup a bucket we can enable _Transfer Accelerate_ option on it and this will give us a _Cloudfront_ endpoint for our S3 bucket, something like :  <u>my-bucket-name.s3-accelerate.amazonaws.com</u>  
Now we can use this endpoint to interact with the bucket and, AWS will behind the scene synch up the data to the S3 bucket.

- ***Static Website using S3***
Amazon S3 provides an easy way to host static websites. Essentially a website that serves up files (HTML pages, that can have CSS and JS if needed). It cannot have any server side code or runtime such as ASP, ASP.net, Servelet or Spring etc.  
In order to do this we simply use the _Static Web Hosting_ option in the _properties_ tab of the S3 bucket.    
This should give us an endpoint such as: <u>http://myBucketName.s3-website-us-east1.amazonaws.com</u>  
Specify the _index document_ (index.html or defualt.html), and the _error document_ (error.html).  
In order for us to access the files within the bucket we would have to make it _public access_ and the contents within it public by configuring the _bucket policy_. The latter can be configured using JSON as shown:
```JSON
{
	"Version": "2012-10-17",
	"Statement": [
		{
			"Sid": "PublicReadGetObject",
			"Effect": "Allow",
			"Principal": "*",
			"Action": [
				"s3:GetObject"
			],
			"Resource": [
				"arn:aws:s3:::myBucketName/*"
			]
		}
	]
}
```  
Now we can upload our souce files (HTML, CSS, JS) and then we are good to go. If we access the resource using the url <u>http://myBucketName.s3-website-us-east1.amazonaws.com</u> it should got the site and the default page (index.html in our case) should be served to the browser.  
Note : Even though we call it static website, the pages can be interactive with client-side code.  
The advantage of using S3 to host content websites is that it can scale automatically and many organizations use this approach if they feel that there might be huge and variable demand.

## EC2 (Elastic Compute Cloud)
==================================================

### EC2 101

#### What is EC2
It is an AWS service that provides resizable compute capacity on demand in the cloud. We can obtain and provision server instances in minutes to scale up or down depending on demand.  
This not only improves the time to scale up or down, but also changes the economics of server infrastructure, as now we can pay for what we use (or provision) rather than heavy upfront capital expenditure. Also typically in the old world we would always overprovision with enough spare capacity that we could grwo into. This would leave us with unused capacity that we had paid for, and eventually fill up till we have to buy again! 

#### EC2 Billing Options
This brings us to the different pricing models that AWS provides for EC2. Each option is designed with different use cases in mind, and one of the importnat skills for architect is to be able to identify the optimal option for a given scenario.  
The various billing options are:  
   - **On-Demand** - This option allows us to pay a fixed rate by the hour (_in the case of Windows servers_) or seconds (_for Linux servers_), without any commitment.
      - Where we need the flexibility without long term commitment.
      - For _workloads_ that are spiky, or unpredictable and cannot be interrupted.
      - Applications that are being developed on AWS for the first time.
      - Keywords - _Variable_ or _Unpredictable_ Workloads, _No Commitments_.

   - **Reserved** - We can sign up for a contract term of 1 Year or 3 years. Whilst this ties us in for the period, we get a significant discount on the hourly rate.
      - This is a good fit for applications that have a known predictable demand.
      - Applications for which we need fixed reserved capacity.
      - Up-front payments and longer terms give us greater discounts
         - For standrad RIs a full up-front payment for 3 year term can give 75% off the on-demand price!
         - For convertible RIs this can be upto 54% off. Convertible RIs give us some flexibility to change some configurations like going from a CPU optimized instance to a Memory optimized instance. The conversion has to result in instances of >= value as the existing.

   - **Spot** - Spot instances allows us to _bid_ a price for some capacity and use it when it is available. This can then be offloaded as well. It is similar to bidding and selling stocks, and works well in situations which affords flexibility in start and end times.
      - Applications that have a huge amount of compute needed (like pharmaceuticals, genomics etc.) but have flexibility in the time they do it.
      - Requires very low compute prices.

   - **Dedicated Hosts** - These are single-tenant hardware deicated to the customer, with configuration they can control. This might be needed if we have softwares that have server-bound licenses.
      - Regulatory requirements might enforce dedicated hardware for a tenant.
      - Some software licenses are hardware bound and cannot be used in a multi-tenant installation.
      - Can be purchased as reservation for upto 70% off the on-demand price. 
      - Tenancy attributes for instances -
         - _default_ - instance runs on shared hardware
         - _dedicated_ - instance runs on _single-tenant_ hardware
         - _host_ - instance runs on dedicated hardware, with _configurations_ the customer _can control_

   - **Dedicated Instances** - We can pay by the hour for instances that run on single-tenant hardware.

   - **Scheduled** - These would be instances that are available on a specified schedule on a recurring basis for a 1 year period.

   - **Capacity Reservation** - Reserve capacity for EC2 instances for any duration in an specific AZ.

#### EC2 Instance Types
When we setup an EC2 instance, the _instance-type_ determines the hardware of the _host_ computer used. The instance types are optimized for different resource configurations such as CPU, memory, storage, IO and are grouped into instance families based on these capabilities.  
The _instance families_ are:  
> 1 - **General Purpose**  
General purpose inatnces are the common standard instance types that provide a balance of _compute_, _memory_, _storage_, _network_ resources and can be used for a variety of workloads.
   - M5, M5a, M5d - _These are based on the Intel Xeon scalable processor or the AMD EPYC processor._ 
   - A1 - _They are the first generation of ARM processor  based instances._
   - T2, T3 - _These instance types provide a baseline level of CPU with the ability to burst to higher levels when required by the workload._

> 2 - **Compute Optimized**  
These instance types are optimized for heavy compte workloads (like data analytics) and have higher ratio of vCPUs and core with higher clock-speeds.
   - C4, C5 - _The latest of the compute optimized category._

> 3 - **Memory Optimized**  
For use cases requiring large RAM (like in-memory data processing or analytics) this family of instance types are best.
   - R4, R5, R5a, R5d - _These are the baseline memory optimized instance type._
   - X1 - _Extremely high memory requirements._
   - Z1 - _They provide high compute along with high memory._

> 4 - **Storage Optimized**  
These instance types provide large local storage within the instance itself. They are best suited for workloads that require high volume/rate of sequential read-write of large data-sets on local storage. They can deliver tens of thousands of IOPS.
   - D2
   - H1
   - I3

> 5 - **Accelerated Computing**  
For workloads that require high performance computing or massive parallel processiing AWS provides instance types that have access to hardware-based compute accelerators like GPUs (Graphichs Processing Units) and FPGAs (Field Programmable Gate Arrays).
   - F1 - _FPGA-based instance type for computationally intensive algorithms._
   - P2, P3 - _GPU-based instance type._
   - G2, G3 - _GPU-based instance type._  

The table below shows a high-level overview of the instance familes with the types of instances and uses cases - 
![EC2-instance-types](EC2-instance-types.png)  
_There are a few mnemonics to help remember these types_ - 
   - gMAT
   - cC
   - mR XZ
   - FPGa
   - DIsH


