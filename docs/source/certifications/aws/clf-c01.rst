CLF-C01 AWS Cloud Practitioner
==============================

+--------------------------------------+------------+
| Domain                               | % of Exam  |
+======================================+============+
| Domain 1: Cloud Concepts             | 26%        |
+--------------------------------------+------------+
| Domain 2: Security and Compliance    | 25%        |
+--------------------------------------+------------+
| Domain 3: Technology                 | 33%        |
+--------------------------------------+------------+
| Domain 4: Billing and Pricing        | 16%        |
+--------------------------------------+------------+
| TOTAL                                | 100%       |
+--------------------------------------+------------+

Domain 1: Cloud Concepts
------------------------

1.1 Define the AWS Cloud and its value proposition
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Cloud is the on demand delivery of IT resources over the internet with pay as you go pricing.

* Define the benefits of the AWS cloud including:
    * Security (Protects your data, accounts and workloads from unauthorized access)
    * Reliability (Little down time, duplication to prevent failure)
    * High Availability (Always up, no single point of failure)
    * Elasticity (don't need to over provision resources up front to handle peak levels, provision the resources you need and you can scale them up or down as required.)
    * Agility (Flexibility of cloud makes it easier to develop and deploy applications, spin up resources in minutes rather than weeks)
    * Pay-as-you go pricing (Only pay for the resources you need, trade fixed expense - upfront servers for variable expense - only pay when you use it)
    * Scalability (Can scale vertically and horizontally, used for varying amount of traffic. Automatically respond to changing demand of resources)
    * Global Reach (Can deploy globally in minutes, all over the world as AWS has data centers everywhere, improved experience and reduces latency)
    * Economy of scale (achieve lower variable rate than on your own, due to having thousands of customers, so becomes less pay as you go pricing)
* Explain how the AWS cloud allows users to focus on business value
    * Shifting technical resources to revenue-generating activities as opposed to managing infrastructure (undifferentiated heavy lifting of IT, common/repetitive tasks and time consuming, aws helps with so we can focus on what will generate business value.)

1.2 Identify aspects of AWS Cloud economics
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
* Define items that would be part of a Total Cost of Ownership proposal
    * Understand the role of operational expenses (OpEx)
    * Understand the role of capital expenses (CapEx)
    * Understand labor costs associated with on-premises operations
    * Understand the impact of software licensing costs when moving to the cloud
* Identify which operations will reduce costs by moving to the cloud
    * Right-sized infrastructure
    * Benefits of automation
    * Reduce compliance scope (for example, reporting)
    * Managed services (for example, RDS, ECS, EKS, DynamoDB)

1.3 Explain the different cloud architecture design principles
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
* Explain the design principles
    * Design for failure (plan for failure, so have redundancy, more instances to take its place)
    * Decouple components versus monolithic architecture (Can scale each part of the system to meet the demand, so don't need more resources than needed, don't wait money. ). Loosely coupled, single failure will not cause cascading failures. (Queue, buffer between the two), Micro services are good.
    * Implement elasticity in the cloud versus on-premises (Able to scale based on demand dynamically which cannot be done on prem as you need to buy the resources and install .etc)
    * Think parallel (Many instances at once can service many requests and once so faster)

well architected framework (self service tool to generate a report)
Operational excellence - ability to run and monitor systems to deliver business value and to continually improve supporting processes and procedures.
Performance efficiency - use computing resources efficiently to meet system requirements
Security - ability to protect info, systems and assets while delivering business value through risk assessments and mitigation strategy
Reliability - ability to recover from infrastructure or service disruptions, dynamically acquire compute resources to meet demand, mitigate disruptions such a mis-config or network issues
cost optimization - run systems to deliver value at lowest price point

Benefits of the cloud:
Trade upfront expense for variable expense.
Benefit from massive economies of scale.
Stop guessing capacity.
Increase speed and agility.
Stop spending money running and maintaining data centers.
Go global in minutes.


Domain 2: Security and Compliance
---------------------------------

2.1 Define the AWS shared responsibility model
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
* Recognize the elements of the Shared Responsibility Model
* Describe the customer's responsibly on  (security in the cloud: os, application and data)
    * Describe how the customer's responsibilities may shift depending on the service used (for example with RDS, Lambda, or EC2)
* Describe AWS responsibilities (Security of the cloud: physical, network and hypervisor)

2.2 Define AWS Cloud security and compliance concepts
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
* Identify where to find AWS compliance information
    * Locations of lists of recognized available compliance controls (for example, HIPPA, SOCs) - AWS artifact get access to compliance reports. Or aws compliance center.
    * Recognize that compliance requirements vary among AWS services
* At a high level, describe how customers achieve compliance on AWS
    * Identify different encryption options on AWS (for example, In transit - being sent, At rest - idle)
* Describe who enables encryption on AWS for a given service
* Recognize there are services that will aid in auditing and reporting
    * Recognize that logs exist for auditing and monitoring (do not have to understand the logs)
    * Define Amazon CloudWatch (monitor and manage various metrics and configure alarm actions based on data on metrics), AWS Config, and AWS CloudTrail (records api calls for account, trail of everything that happens and audits it.)
* Explain the concept of least privileged access

2.3 Identify AWS access management capabilities
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
* Understand the purpose of User and Identity Management
    * Access keys and password policies (rotation, complexity) - Least privileged access - only granted access to aws resources required for current tasks.
    * Multi-Factor Authentication (MFA) - extra layer of security (token too)
    * AWS Identity and Access Management (IAM) (controls access to AWS resources, free, managed Authentication (verify users) and authorization (what user can do))
        * Groups/users - account for user to access AWS resources, group managed permissions for that group.
        * Roles - enables a user or service to assume permissions for a task.
        * Policies, managed policies compared to custom policies - json document, defines permissions for aws iam Identity, defines both aws services the identity can access and what actions can be taken on that service. customer managed or by aws.
    * Tasks that require use of root accounts Protection of root accounts

2.4 Identify resources for security support
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
* Recognize there are different network security capabilities
    * Native AWS services (for example, security groups, Network ACLs - check if packets have permissions to enter/leave subnet, AWS WAF)
    * 3rd party security products from the AWS Marketplace (digital catalog that has thousands of software listings)
* Recognize there is documentation and where to find it (for example, best practices, whitepapers, official documents)
    * AWS Knowledge Center, Security Center, security forum, and security blogs
    * Partner Systems Integrators
* Know that security checks are a component of AWS Trusted Advisor

Domain 3: Technology
--------------------

3.1 Define methods of deploying and operating in the AWS Cloud
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
* Identify at a high level different ways of provisioning and operating in the AWS cloud
    * Programmatic access, APIs, SDKs (interact using programming langs), AWS Management Console (click on site), CLI (make api calls using terminal on my pc), Infrastructure as Code
* Identify different types of cloud deployment models
    * All in with cloud/cloud native (Run all parts of the application in the cloud, migrate existing applications to the cloud, design and build new applications in the cloud. You can build them on low level infrastructure that requires your IT or manage. Alternatively you can build them using higher level services that reduce the management, architecting and scaling requirements of the core infrastructure.)
    * Hybrid (Connect cloud based resources to on prem infrastructure. Integrate cloud based resources with legacy IT Systems, has legacy applications better maintained on promise or due to government requirements to keep certain records on premise.)
    * On-premises or Private (Deploy resources using virtualization and resource management tools, increase resource utilization by using application management and virtualization technologies.)
* Identify connectivity options
    * VPN
    * AWS Direct Connect
    * Public internet

3.2 Define the AWS global infrastructure
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
* Describe the relationships among Regions, Availability Zones, and Edge Locations
    * High availability and fault tolerance
    * Region - areas in world where data center is. Likely to be where they are needed
    * Availability zones - single data center or group of them. All in an area makes a region
    * Edge locations - site that use cloudfront to store cached copies of your content closer to your customers.
* Describe how to achieve high availability through the use of multiple Availability Zones
    * Recall that high availability is achieved by using multiple Availability Zones
    * Recognize that Availability Zones do not share single points of failure
* Describe when to consider the use of multiple AWS Regions
    * Disaster recovery/business continuity
    * Low latency for end-users
    * Data sovereignty
* Describe at a high level the benefits of Edge Locations (closer to users so faster.)
    * Amazon CloudFront
    * AWS Global Accelerator

3.3 Identify the core AWS services
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
* Describe the categories of services on AWS (compute - allows you to carry out computational activities, storage - allows you to store your data/files, network - interact between different resources, database - way to store your processed data)
* Identify AWS compute services
    * Recognize there are different compute families
    * Recognize the different services that provide compute (for example, AWS Lambda compared to Amazon Elastic Container Service (Amazon ECS), or Amazon EC2, etc.) (Amazon Elastic compute cloud (EC2), virtual servers, they are highly flexible, cost effective and quick compared to own servers., share host with multiple other instances or vms and hypervisor shares the resources (multi tenancy)), Serverless - Run code on servers but don't need to provision (AWS lambda configure trigger and runs code when triggered, suitable for quick processing), Elastic container service (package for your code), or elastic kubernetes service, aws fargate serverless for ecs or eks. serverless - short running, even based no provisioning, else ec2.
    * Recognize that elasticity is achieved through Auto Scaling (Use Amazon EC2 auto scaling, dynamic - responds to changing demand, prejudice schedules amount based on predicted demand, can use both together to scale faster, scale up (more compute/mem), scale out (more instances), new instances where needed and terminated when no longer needed)
    * Identify the purpose of load balancers (Elastic load balancing, automatically distributes incoming traffic across multiple resources)
* Identify different AWS storage services
    * Describe Amazon S3 (simple storage service, store and retrieve unlimited data, store data as objects in buckets.)
    * Describe Amazon Elastic Block Store (Amazon EBS) - create virtual hard drives using block level storage (not tied to host like instance stores are)
    * Describe Amazon S3 Glacier (archive data)
    * Describe AWS Snowball (physical device to transport up to exabytes of data in and out of AWS)
    * Describe Amazon Elastic File System (Amazon EFS) - Linux file system that has many instances read or writing at once. This is a scalable file system. It grows and shrinks Automatically
    * Describe AWS Storage Gateway (hybrid cloud storage service)
* Identify AWS networking services
    * Identify VPC - allows you to establish boundaries around your aws resources (Amazon Virtual Private cloud VPC, internet gateway required to allow access from internet, virtual private gateway only allows access from an approved network) subnets is a section of a vpc that can contain resources
    * Identify security groups (around instances EC2 prevents everything by default, needs to be modified to accept specific types of requests) has state so can remember
    * Identify the purpose of Amazon Route 53 (domain name service DNS, translation service, converts website names to ip addresses and routes your browser to it)
    * Identify VPN, AWS Direct Connect (private dedicated connection from your data center to aws)
* Identify different AWS database services
    * Install databases on Amazon EC2 compared to AWS managed databases
    * Identify Amazon RDS (Relational database service) - data stored in a way which that it relates to each other.
    * Identify Amazon DynamoDB - serverless database (non relational key-value pair), create tables to store and create data
    * Identify Amazon Redshift (data warehousing service for big data analytics)

3.4 Identify resources for technology support
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
* Recognize there is documentation (best practices, whitepapers, AWS Knowledge Center, forums, blogs)
* Identify the various levels and scope of AWS support
    * AWS Abuse
    * AWS support cases
    * Premium support
    * Technical Account Managers
* Recognize there is a partner network (marketplace, third-party) including Independent Software Vendors and System Integrators
* Identify sources of AWS technical assistance and knowledge including professional services, solution architects, training and certification, and the Amazon Partner Network
* Identify the benefits of using AWS Trusted Advisor (inspects your environment against pillars, does checks based on best practices. Can save you money, improve security, performance .etc )

Domain 4: Billing and Pricing
-----------------------------

4.1 Compare and contrast the various pricing models for AWS (for example, On-Demand Instances, Reserved Instances, and Spot Instance pricing)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
* Identify scenarios/best fit for On-Demand Instance pricing (To get started and test out ideas, baseline for average usage, short term irregular workloads that cannot be interrupted, no upfront costs or min contracts, run until you stop them and pay for what you use)
* Identify scenarios/best fit for Reserved-Instance pricing (Good for predictable usage and about 75% discount)
    * Describe Reserved-Instances flexibility
    * Describe Reserved-Instances behavior in AWS Organizations
* Identify scenarios/best fit for Spot Instance pricing (Spare capacity, 90% discount, work flow can handle being terminated, batch workloads. flexible start and end times)
* Saving plan - fix cost for 1/3 years and can get about 70% cheaper
* Dedicated - host just for you

4.2 Recognize the various account structures in relation to AWS billing and pricing
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
* Recognize that consolidated billing is a feature of AWS Organizations
* Identify how multiple accounts aid in allocating costs across departments (can get a bulk discount for all accounts)

4.3 Identify resources available for billing support
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
* Identify ways to get billing support and information
    * Cost Explorer (tool to visualize, understand and manage AWS costs and usage over time), AWS Cost and Usage Report, Amazon QuickSight, third-party partners, and AWS Marketplace tools
    * Open a billing support case
    * The role of the Concierge for AWS Enterprise Support Plan customers
* Identify where to find pricing information on AWS services
    * AWS Simple Monthly Calculator (lets you estimate costs of your use cases on AWS)
    * AWS Services product pages
    * AWS Pricing API
* Recognize that alarms/alerts exist
* Identify how tags are used in cost allocation (user defined key value pairs, can filter by tag to see expenses related to them)

Appendix
--------

Which key tools, technologies, and concepts might be covered on the exam?
The following is a non-exhaustive list of the tools and technologies that could appear on the exam. This list is subject to change and is provided to help you understand the general scope of services, features, or technologies on the exam. The general tools and technologies in this list appear in no particular order.
AWS services are grouped according to their primary functions. While some of these technologies will likely be covered more than others on the exam, the order and placement of them in this list are no indication of relative weight or importance:

* APIs
* Cost Explorer
* AWS Cost and Usage Report
* AWS Command Line Interface (CLI)
* Elastic Load Balancers
* Amazon EC2 instance types (for example, Reserved, On-Demand, Spot)
* AWS global infrastructure (for example, AWS Regions, Availability Zones)
* Infrastructure as Code (IaC)
* Amazon Machine Images (AMIs)
* AWS Management Console
* AWS Marketplace
* AWS Professional Services
* AWS Personal Health Dashboard
* Security groups
* AWS Service Catalog
* AWS Service Health Dashboard
* Service quotas
* AWS software development kits (SDKs)
* AWS Support Center
* AWS Support tiers
* Virtual private networks (VPNs)

AWS services and features
~~~~~~~~~~~~~~~~~~~~~~~~~

Analytics:

* Amazon Athena (query large scale data on s3)
* Amazon Kinesis
* Amazon QuickSight (Business intelligence service enabling dashboards)

Application Integration:

* Amazon Simple Notification Service (Amazon SNS) - Publish/subscribe channel, notify many listeners at once.
* Amazon Simple Queue Service (Amazon SQS) - Send, store, receive messages between components at any volume. Payload (data in message)

Compute and Serverless:

* AWS Batch
* Amazon EC2
* AWS Elastic Beanstalk (you provide code and config, and then this deploys resources needed to perform the tasks add just capacity, load balancing, automatic scaling and application health monitoring)
* AWS Lambda
* Amazon Lightsail
* Amazon WorkSpaces

Containers:

* Amazon Elastic Container Service (Amazon ECS)
* Amazon Elastic Kubernetes Service (Amazon EKS)
* AWS Fargate

Database:

* Amazon Aurora (enterprise relation database) it is very fast.
* Amazon DynamoDB
* Amazon ElastiCache
* Amazon RDS
* Amazon Redshift

Developer Tools:

* AWS CodeBuild
* AWS CodeCommit
* AWS CodeDeploy
* AWS CodePipeline
* AWS CodeStar

Customer Engagement:

* Amazon Connect

Management, Monitoring, and Governance:

* AWS Auto Scaling
* AWS Budgets (create budget to plan your usage, service costs and instance reservations)
* AWS CloudFormation (infrastructure as code tool, allows you to define aws resources using json or yaml with cloud formation templates, you define what you want and it will spin them up for you, it is like terraform)
* AWS CloudTrail
* Amazon CloudWatch
* AWS Config
* AWS Cost and Usage Report
* Amazon EventBridge (Amazon CloudWatch Events)
* AWS License Manager
* AWS Managed Services
* AWS Organizations (central location to manage many AWS accounts)
* AWS Secrets Manager
* AWS Systems Manager
* AWS Systems Manager Parameter Store
* AWS Trusted Advisor

Networking and Content Delivery:

* Amazon API Gateway
* Amazon CloudFront
* AWS Direct Connect
* Amazon Route 53
* Amazon VPC

Security, Identity, and Compliance:

* AWS Artifact
* AWS Certificate Manager (ACM)
* AWS CloudHSM
* Amazon Cognito (managed service that allows you to handle authentication and aspects of authorization for custom web and mobile apps through aws)
* Amazon Detective
* Amazon GuardDuty (provides intelligent threat detection for AWS infrastructure and resources)
* AWS Identity and Access Management (IAM)
* Amazon Inspector (perform automated security assessments against your resources .etc)
* AWS License Manager
* Amazon Macie
* AWS Shield (service that protects against DDos Attacks)
* AWS WAF (web app firewall)

Storage:

* AWS Backup
* Amazon Elastic Block Store (Amazon EBS)
* Amazon Elastic File System (Amazon EFS)
* Amazon S3
* Amazon S3 Glacier
* AWS Snowball Edge
* AWS Storage Gateway


Other:
AWS Outposts - aws in effect installs a mini region installed in your server
