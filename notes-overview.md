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
5) CodePipeline - CI/CD pipeline to wire up the rest of teh deve-tools services.
6) X-Ray - Debug and analyze serverless apps. Request tracing.
7) Cloud9 - IDE on the cloud via the brwoser.

### C


