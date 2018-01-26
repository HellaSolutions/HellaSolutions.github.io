---
layout: "post"
title: "1 AWS Services Overview"
date: "2018-01-18 11:43"
---

# AWS Overview

## AWS Global Infostructure

1. **Avialability Zone**: one or multiple data centers
2. **Regions**: Geographical region containing two or more Avialability Zones in replica
3. Edge Locations: endpoints used to cache content (Content Delivery Network). Tipically **CloudFront**,
the Amazon CDN
4. The number of Edge Locations is greater than the number of Regions (about x 10 factor)

## Service Group: Compute

- <span style="color:black;background-color:#FFF8DC">EC2</span>: Amazon **Elastic Compute Cloud** provides scalable computing capacity in the AWS cloud. You can use Amazon EC2 to launch as many or as few virtual servers as you need, configure security and networking, and manage storage. Amazon EC2 enables you to scale up or down to handle changes in requirements or spikes in popularity, reducing your need to forecast traffic.

- <span style="color:black;background-color:#FFF8DC">ECS</span>: **Elastic Container Service** makes it easy to deploy, manage, and scale **Docker** containers running applications, services, and batch processes. Amazon ECS places containers across your cluster based on your resource needs and is integrated with familiar features like Elastic Load Balancing, EC2 security groups, EBS volumes and IAM roles.

- <span style="color:black;background-color:#FFF8DC">Elastic Beanstalk</span>: With Elastic Beanstalk, you can quickly deploy and manage applications in the AWS Cloud without worrying about the infrastructure that runs those applications. You simply upload your application, and Elastic Beanstalk automatically handles the details of capacity provisioning, load balancing, scaling, and application health monitoring. Elastic Beanstalk uses highly reliable and scalable services that are available in the **AWS Free Tier**
- <span style="color:black;background-color:#FFF8DC">Lambda Functions</span>: AWS Lambda is a compute service that lets you run code **without provisioning or managing servers**. AWS Lambda executes your code only when needed and **scales automatically**, from a few requests per day to thousands per second. You pay only for the compute time you consume. AWS Lambda runs your code on a high-availability compute infrastructure and performs all of the administration of the compute resources, including server and operating system maintenance, capacity provisioning and automatic scaling, code monitoring and logging. All you need to do is supply your code in one of the languages that AWS Lambda supports (currently Node.js, Java, C#, Go and Python).
You can use AWS Lambda to run your code in **response to events**, such as changes to data in an Amazon S3 bucket or an Amazon DynamoDB table; to run your code in response to HTTP requests using Amazon API Gateway; or invoke your code using API calls made using AWS SDKs. With these capabilities, you can use Lambda to easily build **data processing triggers** for AWS services like Amazon S3 and Amazon DynamoDB process streaming data stored in Kinesis, or create your own back end that operates at AWS scale, performance, and security.
You can also build **serverless applications** composed of functions that are triggered by events and automatically deploy them using AWS CodePipeline and AWS CodeBuild. For more information, see Deploying Lambda-based Applications.
- <span style="color:black;background-color:#FFF8DC">LightSail</span>:simplified small business Internet Service Provider
- <span style="color:black;background-color:#FFF8DC">Batch</span>: enables you to easily and efficiently run batch computing workloads of any scale on using **EC2** and **EC2 Spot**.

## Service Group: Storage

- <span style="color:black;background-color:#FFF8DC">S3</span>: **Simple Storage Service** is storage for the Internet. You can to store and retrieve any amount of data at any time, from anywhere on the web.
- <span style="color:black;background-color:#FFF8DC">EFS</span>: **Elastic File System** provides simple, scalable file storage for use with **EC2**. The storage capacity is elastic, growing and shrinking automatically as you add and remove files, so applications have the storage they need, when they need it. supports
  - NFSv4
  - Portable Operating System Interface (POSIX) permissions
  - Scalable, highly available, and highly durable
  - Encryption
- <span style="color:black;background-color:#FFF8DC">Glacier</span>: extremely low-cost storage service that provides secure, durable, and flexible storage for data **backup** and **archival**
- <span style="color:black;background-color:#FFF8DC">Storage Gateway</span>: is a service connecting an **on-premises software appliance with cloud-based storage** to provide seamless and secure integration between an organization's on-premises IT environment and AWS's storage infrastructure

## Service Group: Databases

- <span style="color:black;background-color:#FFF8DC">RDS</span>: provides relational database instances, it is possible to choose among
  - Amazon Aurora (Amazon MySQL version)
  - MySQL
  - Postgres
  - Oracle
  - SQL Server
- <span style="color:black;background-color:#FFF8DC">DynamoDB</span>: provides instances based on the highly available **key-value structured storage** (distributed data store) **Dynamo**.
- <span style="color:black;background-color:#FFF8DC">ElasticCache</span>: launch, manage, and scale a distributed in-memory cache in the cloud. Supported **Redis**, **Memcache**.
- <span style="color:black;background-color:#FFF8DC">RedShift</span>: fully managed, **petabyte-scale data warehouse solution** that makes it simple and cost-effective to efficiently analyze all your data using your existing business intelligence tools.

## Service Group: Migration

- <span style="color:black;background-color:#FFF8DC">MigrationHub</span>: provides a single place to discover your existing servers, plan migrations, and track the status of each application migration. It provides visibility into your application portfolio and streamlines **planning** and **tracking**. You can see the status of the servers and databases that make up each of the applications you are migrating regardless of which migration tool you are using (based in on premise installed agents).
- <span style="color:black;background-color:#FFF8DC">Application Discovery Service</span>: helps systems integrators quickly and reliably plan application migration projects by **automatically identifying applications running in on-premises data centers**, their associated dependencies, and their performance profile.
- <span style="color:black;background-color:#FFF8DC">Database Migration Service</span>: migration tool with SQL source code and schemas ispector
- <span style="color:black;background-color:#FFF8DC">Server Migration Service</span>: automates the migration of on-premises **VMware vSphere** or **Microsoft Hyper-V/SCVMM** **virtual machines** to AWS. It incrementally replicates on-premises server VMs as cloud-hosted **Amazon Machine Images** (**AMIs**) ready for deployment on Amazon **EC2**. Working with AMIs, you can easily test and update your cloud-based images before deploying them in production.
- <span style="color:black;background-color:#FFF8DC">Snowball</span>: service that accelerates transferring large amounts of data into and out of AWS using **physical storage appliances, bypassing the Internet**. Each AWS Snowball appliance (>= 50Tb) type can transport data at faster-than internet speeds. This transport is done by shipping the data in the appliances through a regional carrier. The appliances are rugged shipping containers, complete with E Ink shipping labels.

## Service Group: Network and Content Security

- <span style="color:black;background-color:#FFF8DC">VPC</span>: **Virtual Private Cloud*** is a virtual network that closely resembles a traditional network that you'd operate in your own data center, with the benefits of using the scalable infrastructure of AWS. For example, you can have an Amazon EC2 instance running in a VPC that you can access from the Internet using **SSH** (for Linux instances) or **Remote Desktop** (for Windows instances)
- <span style="color:black;background-color:#FFF8DC">CloudFront</span>: **Content Delivery Network**
- <span style="color:black;background-color:#FFF8DC">API delivery gateway</span>: Amazon API Gateway is an AWS service that enables developers to create, publish, maintain, monitor, and secure APIs at any scale. You can create APIs that access AWS or other web services, as well as data stored in the AWS Cloud.In practical terms, API Gateway lets you create, configure, and host a **RESTful API** to enable applications to access the AWS Cloud. For example, an application can call an API in API Gateway to upload a user's annual income and expense data to Amazon S3 or Amazon DynamoDB, process the data in AWS Lambda to compute tax owed, and file a tax return via the IRS website.

![Backplane architecture](/_posts/2018/BackplaneArch.png)

- <span style="color:black;background-color:#FFF8DC">Direct Connect</span>: makes it easy to establish a **dedicated network connection** from your premises to AWS. Using AWS Direct Connect, you can establish private connectivity between AWS and your datacenter, office, or colocation environment, which in many cases can reduce your network costs, increase bandwidth throughput, and provide a more consistent network experience than Internet-based connections (**VLAN 802.1q**).

## Service Group: Developer Tools

- <span style="color:black;background-color:#FFF8DC">CodeStar</span>: is a cloud-based service for creating, managing, and working with software development projects on AWS An AWS CodeStar project creates and **integrates AWS services for your project development toolchain**. Depending on your choice of AWS **CodeStar project template**, that toolchain might include **source control**, **build**, **deployment**, **virtual servers** or **serverless resources**, and more. AWS CodeStar also **manages the permissions** required for team members. By adding users as team members to an AWS CodeStar project, project owners can quickly and simply grant each team member role-appropriate access to a project and its resources.
- <span style="color:black;background-color:#FFF8DC">CodeCommit</span>: version control service hosted by Amazon Web Services that you can use to privately store and manage assets (such as documents, source code, and binary files) in the cloud
- <span style="color:black;background-color:#FFF8DC">CodeBuild</span>: fully managed **build service** in the cloud. AWS CodeBuild compiles your source code, runs unit tests, and produces artifacts that are ready to deploy. It eliminates the need to provision, manage, and scale your own build servers. It provides prepackaged build environments for the most popular programming languages and build tools such as **Apache Maven**, **Gradle**, and more. You can also customize build environments in AWS CodeBuild to use your own build tools. AWS CodeBuild scales automatically to meet peak build requests.
- <span style="color:black;background-color:#FFF8DC">CodeDeploy</span> **deployment service** that automates application deployments to **Amazon EC2** instances, **on-premises instances**, or **serverless Lambda functions**.
You can deploy a nearly unlimited variety of application content, such as code, serverless AWS Lambda functions, web and configuration files, executables, packages, scripts, multimedia files, and so on. AWS CodeDeploy can deploy application content that runs on a server and is **stored in Amazon S3 buckets, GitHub repositories, or Bitbucket repositories**. You do not need to make changes to your existing code before you can use AWS CodeDeploy.
- <span style="color:black;background-color:#FFF8DC">CodePipeline</span>
**continuous delivery service** you can use to **model**, **visualize**, and **automate** the steps required to release your software. You can quickly model and configure the different stages of a software release process. AWS CodePipeline automates the steps required to release your software changes continuously.
- <span style="color:black;background-color:#FFF8DC">Cloud9</span> Internet/on-premise development IDE
- <span style="color:black;background-color:#FFF8DC">X-Ray</span> makes it easy for developers to analyze the **behavior of their distributed applications** by providing request **tracing**, **exception collection**, and **profiling** capabilities.

 ## Service Group: Management Tools

- <span style="color:black;background-color:#FFF8DC">CloudWatch</span> **monitors AWS resources and the applications you run on AWS in real time**. You can use CloudWatch to collect and track metrics, which are variables you can measure for your resources and applications. CloudWatch **alarms** send notifications or **automatically make changes to the resources you are monitoring based on rules that you define**. For example, you can monitor the CPU usage and disk reads and writes of your Amazon EC2 instances and then use this data to determine whether you should launch additional instances to handle increased load. You can also use this data to stop under-used instances to save money. In addition to monitoring the built-in metrics that come with AWS, you can monitor your own **custom metrics**. With CloudWatch, you gain system-wide visibility into **resource utilization**, **application performance**, and **operational health**.
- <span style="color:black;background-color:#FFF8DC">CloudFormation</span> is a **declarative (YAML/JSON) and visualizable framework** that allows you to quickly and easily deploy your infrastructure resources and applications on AWS. You can use one of the **templates** we provide to get started quickly with applications like WordPress or Drupal, one of the many sample templates or create your own template.
- <span style="color:black;background-color:#FFF8DC">CloudTrial</span> helps you enable **governance**, **compliance**, and **operational and risk auditing** of your **AWS account**. Actions taken by a user, role, or an AWS service are recorded as events in CloudTrail. Events include actions taken in the AWS Management Console, AWS Command Line Interface, and AWS SDKs and APIs.
Visibility into your AWS account activity is a** key aspect of security and operational best practices**. You can use CloudTrail to view, search, download, archive, analyze, and respond to account activity across your AWS infrastructure. You can identify who or what took which action, what resources were acted upon, when the event occurred, and other details to help you analyze and respond to activity in your AWS account.
- <span style="color:black;background-color:#FFF8DC">Config</span> provides a detailed view of the **configuration of AWS resources in your AWS account**. This includes **how the resources are related to one another** and **how they were configured in the past** so that you can see how the configurations and relationships change over time. An AWS resource is an entity you can work with in AWS, such as an Amazon Elastic Compute Cloud (EC2) instance, an Amazon Elastic Block Store (EBS) volume, a security group, or an Amazon Virtual Private Cloud (VPC).
- <span style="color:black;background-color:#FFF8DC">OpsWorks</span> is a **configuration management service** that helps you configure and operate applications in a cloud enterprise by using **Puppet** or **Chef**. AWS OpsWorks Stacks and AWS OpsWorks for Chef Automate let you use Chef cookbooks and solutions for configuration management, while AWS OpsWorks for Puppet Enterprise lets you configure a Puppet Enterprise master server in AWS. Puppet offers a set of tools for enforcing the desired state of your infrastructure, and automating on-demand tasks.
- <span style="color:black;background-color:#FFF8DC">Service Catalog</span> allows organizations to **create and manage catalogs of IT services** that are **approved** for use on AWS. These IT services can include everything from virtual machine images, servers, software, and databases to complete multi-tier application architectures. AWS Service Catalog allows organizations to centrally manage commonly deployed IT services, and helps organizations achieve **consistent governance** and **meet compliance requirements**, while enabling users to quickly deploy only the approved IT services they need with the constraints your organization sets (Fortune's 500).
- <span style="color:black;background-color:#FFF8DC">System Manager</span> (formerly Amazon EC2 Systems Manager) is a unified interface that allows you to easily **centralize operational data** and **automate tasks** across your AWS resources. Systems Manager shortens the time to detect and resolve **operational problems** in your infrastructure. Systems Manager gives you a complete **view of your infrastructure performance and configuration**, simplifies resource and application management, and makes it easy to operate and manage your infrastructure at scale.
- <span style="color:black;background-color:#FFF8DC">Trusted Advisor</span> provides advices and alerts across multiple disciplines: save money, security, performance, etc.
- <span style="color:black;background-color:#FFF8DC">Managed Services</span> delivers consistent operations management and predictable results by following **ITIL® best practices**, and provides tooling and automation to increase efficiency, and reduce your operational overhead and risk.

## Service Group: Media Services

- <span style="color:black;background-color:#FFF8DC">Elastic Transcoder</span> lets you convert digital media stored in **S3** into the audio and video codecs and the containers required by consumer playback devices. For example, you can convert large, high-quality digital media files into formats that users can play back on mobile devices, tablets, web browsers, and connected televisions. Elastic Transconder presents three major components
  - **Pipelines**: are **queues** that manage your transcoding jobs. Elastic Transcoder begins to process jobs in the order in which you add them to a pipeline. Typically, you’ll create at least two pipelines, one for standard-priority jobs and one for high-priority jobs. Most jobs go into the standard-priority pipeline; you use the high-priority pipeline only when you need a file to be transcoded immediately
  - **Presets**: is a **template** that contains the settings that you want Elastic Transcoder to apply during the transcoding process, for example, the number of audio channels and the video resolution that you want in the transcoded file
  - **Jobs**: does the work of transcoding a media file from one format into another format. When you create a job, you specify the information that Elastic Transcoder needs to perform the transcoding: which file to transcode, what to name the transcoded file, which preset to use
- <span style="color:black;background-color:#FFF8DC">Media Convert</span> is a file-based video processing service that provides scalable video processing for content owners and distributors with media libraries of any size. It offers advanced features that enable premium content experiences, including:
  - professional broadcast codecs that support increased bit depth and HDR content creation
  - still graphic overlays
  - advanced audio
  - digital rights management (DRM)
  - closed captioning support
- <span style="color:black;background-color:#FFF8DC">Media Live</span> is a real-time video service that lets you easily create live outputs for broadcast and streaming delivery. Offers multi-availability zone architecture for inputs, channels, and outputs for highly available service within a region. The service supports elastic resource allocation for channels and automatic recovery of channels after any failure detection.
- <span style="color:black;background-color:#FFF8DC">Media Package</span> offers a broadcast-grade viewing experience for viewers, while allowing you the flexibility to control and protect your content. Additionally, the built-in resiliency and scalability of AWS Elemental MediaPackage means that you have the right amount of resources at the right time, with no manual intervention required.
-  <span style="color:black;background-color:#FFF8DC">Media Store</span> is a video origination and storage service that offers the high performance, predictable low latency, and immediate consistency required for live origination. With AWS Elemental MediaStore, you can manage video assets as objects in containers to build dependable, cloud-based media workflows.
- <span style="color:black;background-color:#FFF8DC">Media Tailor</span> ad insertion service that runs in the AWS Cloud. With AWS Elemental MediaTailor, you can serve targeted ads to viewers while maintaining broadcast quality in over-the-top (OTT) video applications
- <span style="color:black;background-color:#FFF8DC">Kinesis Video Streams</span> You can use Kinesis Video Streams to capture **massive amounts of live video data from millions of sources**, including smartphones, security cameras, webcams, cameras embedded in cars, drones, and other sources. You can also send non-video time-serialized data such as audio data, thermal imagery, depth data, RADAR data, and more. As live video streams from these sources into a Kinesis video stream, you can build applications that can access the data, frame-by-frame, in real time for low-latency processing (E.g. Machine Learning applications)

## Service Group: Machine Learning

- <span style="color:black;background-color:#FFF8DC">Media Live</span> is a fully managed machine learning service. With Amazon SageMaker, data scientists and developers can quickly and easily build and train machine learning models, and then directly deploy them into a production-ready hosted environment.
- <span style="color:black;background-color:#FFF8DC">Comprehend</span> is a continuously-trained natural language processing service. It’s free to try and easy to get started analyzing unstructured text like customer reviews and news articles.
- <span style="color:black;background-color:#FFF8DC">Deep Lens</span> is a deep leaning enabled video camera
- <span style="color:black;background-color:#FFF8DC">Lex</span> is a service for building conversational interfaces using voice and text
- <span style="color:black;background-color:#FFF8DC">Rekognition</span> Deep learning-based visual analysis service. Search, verify, and organize millions of images and video
- <span style="color:black;background-color:#FFF8DC">Transcribe</span> from speech to text
- <span style="color:black;background-color:#FFF8DC">Polly</span> from text to speech
- <span style="color:black;background-color:#FFF8DC">Translate</span> translation service

## Service Group: Analytics
- <span style="color:black;background-color:#FFF8DC">Athena</span> is a fast, cost-effective, serverless interactive query service that makes it easy to analyze **petabytes of data in S3** with no data warehouses or clusters to manage
- <span style="color:black;background-color:#FFF8DC">EMR (Elastic MapReduce)</span> analyze and process vast amounts of data. It does this by distributing the computational work across an Haddop managed cluster of virtual servers running in the Amazon cloud.
- <span style="color:black;background-color:#FFF8DC">CloudSearch</span>  search service for large collections of data such as web pages, document files, forum posts, or product information. You can quickly add search capabilities without having to become a search expert or worry about hardware provisioning, setup, and maintenance. As your volume of data and traffic fluctuates, CloudSearch scales to meet your needs.
- <span style="color:black;background-color:#FFF8DC">Elastic Search Service</span> managed service that makes it easy to create a domain and deploy, operate, and scale Elasticsearch clusters in the AWS Cloud. Elasticsearch is a popular open-source search and analytics engine for use cases such as log analytics, real-time application monitoring, and clickstream analytics. With Amazon ES, you get direct access to the Elasticsearch APIs so that existing code and applications work seamlessly with the service.
- <span style="color:black;background-color:#FFF8DC">Kinesis</span> real-time analytics for data streaming. Presents four versions
  - **Data Streams**: collects and processes large streams of data records in real time
  - **Data Firehose**: fully managed service for delivering real-time streaming data to destinations such as Amazon Simple Storage Service (Amazon S3), Amazon Redshift, Amazon Elasticsearch Service (Amazon ES), and Splunk
  - **Data Analytics**: processes and analyzes streaming data using standard SQL
  - **Video Streams**:  fully managed AWS service that you can use to stream live video from devices to the AWS Cloud, or build applications for real-time video processing or batch-oriented video analytics
-  <span style="color:black;background-color:#FFF8DC">QuickSight</span> Amazon Business Intelligence tool
-  <span style="color:black;background-color:#FFF8DC">Pipeline</span> service that that automates the movement and transformation of data. With AWS Data Pipeline, you can define data-driven workflows, so that tasks can be dependent on the successful completion of previous tasks. You define the parameters of your data transformations and AWS Data Pipeline enforces the logic that you've set up.
-  <span style="color:black;background-color:#FFF8DC">Glue</span> fully managed ETL (extract, transform, and load) service that makes it simple and cost-effective to categorize your data, clean it, enrich it, and move it reliably between various data stores.
