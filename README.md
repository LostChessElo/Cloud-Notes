# CLOUD 101 NOTES 
All notes taken from aws educate 
---
## WHAT IS CLOUD COMPUTING?
The on-demand delivery of IT resources over the internet with pay-as-you-go pricing 
- **on-demand delivery** is when a cloud provider has the resources you need when you need them 
- **IT resources over the internet** can refer to; Servers, Networks, development tools and applications 
-  **Pay-as-you-go pricing** refers to paying for what you use when you use it.
---

## BENEFITS OF CLOUD COMPUTING
- **Trade upfront expenses for variable expenses**: instead of paying for resources you need to invest in before using, you pay only for computing resources you use (variable expense) 
- **Stop spending money to run and maintain data centers**: Computing in data centers requires you to spend more time and money managing infrastructure, cloud computing shifts your focus away from these tasks and more on your application and users
- **Stop guessing capacity**: With cloud computing you don't have to guess how much infrastructure capacity you'll need before deploying an application 
- Benefit from massive economies of scale: By using cloud computing you can lower variable cost much more than what you could on your own.Because usage from a large pool of users can aggregate in the cloud, providers are able to achieve much larger economy of scale.
- **Increase speed and agility**: The flexibility of the cloud provides you with more time to experiment and innovate. The cloud gives you access to new resources within minutes
- **Go global in minutes**: Deploy applications to customers worldwide quickly at low latency,  
---

## CLOUD SERVICE MODELS 
- **IaaS**: Infrastructure as a Service provides access to data storage space 
 networking features and computers (digital and hardware) 
 examples: EC2, S3, RDS and Route 53
- **PaaS**: Platform as a Service removes the need for organizations to manage and maintain underlying infrastructure and rather shift focus to deployment and management of applications 
examples: AWS Elastic Beanstalk - for quickly deploying and scaling applications 
- **SaaS**: Software as a Service is the completed product the service manager provides and maintains, you do not worry about how the underlying infrastructure is managed or how the service is maintained 
examples: video meeting sites, email sites, file sharing sites and messaging apps
---

## CLOUD DEPLOYMENT MODELS 

- **Cloud**: migrate existing software to the cloud or design new software in the cloud, they can either be built low level in which infrastructure, architecture and scaling requirements must be managed, or high level approach that abstract these requirements to a degree 
example: A company builds an application consisting of virtual servers, databases and networking components all existing in the cloud 
- **Hybrid**: Cloud-based resources connected to on-premises infrastructure 
---
# AWS OFFERINGS

- **Compute**
- **Storage**
- **Databases**
- **Networking and content delivery**
- **Developer tools**
- **Business applications**
- **Management and governance**
- **Machine learning**
- **Internet of Things**
- **Security, identity and compliance**

---

# REGIONS

- **Regions:** Physical location where data centers are clustered together, a group of logical data centers are called an **Availability Zone (AZ)**. Each AWS region consists of multiple isolated and physically separate **AZ's** within a geographic area.

---

# AVAILABILITY ZONES

- **Availability Zones (AZ's)** are areas within a region consisting of data centers (typically **3**) and house all the hardware AWS offers.
- **AZ's** are physically separate by a meaningful distance (**~100 km**) from other AZ's.
- They are interconnected with **high-bandwidth, low-latency networking**, to provide low-latency networking between zones that is sufficient to accomplish **synchronous replication (same time replication).**

---

# EDGE LOCATIONS

- Connected to regions through the **AWS network** across the globe.
- Link with **tens of thousands of networks** for dynamic content acceleration and improved origin fetches.
- **Edge locations** cache copies of your content for faster delivery to users.
- Supports AWS services like **Route 53** and **Amazon CloudFront**.
- AWS has **over 200 edge locations** placed in **90 cities across 47 countries**.

---

# PLANNING FOR FAILURE

### Storage

- When a file is stored in **Amazon S3 (Simple Storage Service)** the file is redundantly copied into every **Availability Zone** within the region in case of one going down.

### Computing

- It is **best practice** to spread out computing resources across multiple **Availability Zones** to guarantee **high availability**. In the case that an **Availability Zone** goes down, the application stays running.

### Databases

- You can configure your database with **Multi-AZ deployment**. If your **Availability Zone** with the primary database fails, then one of the databases in a healthy **Availability Zone** becomes your primary.

---

# GLOBAL INFRASTRUCTURE BENEFITS

### Performance

- Offers **high-performance, low-latency infrastructure** with virtually unlimited capacity, meaning **high availability**.

### Availability

- Designed for **physical redundancy**, providing uninterrupted performance even in the event of a power outage, internet downtime, floods or any other natural disaster.

### Security

- Monitored **24/7** to ensure **confidentiality, integrity and availability** of user data.
- Can encrypt, migrate and manage retention on data.

### Reliability

- Designed and built for **redundancy and reliability**, from regions to networking links to load balancers to routers to firmware.

### Scalability

- Cloud is **virtually infinitely scalable**. Companies can access resources when they need them within minutes and deploy hundreds or even thousands of servers in minutes.

### Low Cost

- Companies are able to reduce the **Total Cost of Ownership (TCO)** of their overall IT infrastructure by leveraging the cloud.

---

# AWS SHARED RESPONSIBILITY

> **AWS is responsible for the security OF the cloud while a user/company is responsible for their security IN the cloud.**

- A company may be responsible for security requirements for their content. For example, if they create an **S3 bucket** the user is responsible for any access and encryption needed.

### AWS is responsible for:

- Physical security of data centers.
- Hardware and software infrastructure.
- Network infrastructure.
- Virtualization infrastructure.

So in the **S3** example, AWS is responsible for storage hardware maintenance and physical security of the data centers.

---

# AWS WELL-ARCHITECTED FRAMEWORK

## Operational Excellence

The ability to run and monitor systems to deliver business value and to continually improve supporting processes and procedures.

### Design processes include:

- Performing operations as code.
- Annotating documentation.
- Anticipating failure.
- Frequently making small reversible changes.

---

## Security

The ability to protect information, systems and assets while delivering business value through risk assessments and mitigation strategies.

### Best practices:

- Automate security best practices when possible.
- Apply security to all layers.
- Protect data in transit and at rest.

---

## Reliability

The ability of a system to:

- Recover from infrastructure or service disruptions.
- Dynamically acquire resources to meet demand.
- Mitigate disruptions.

Also includes:

- Testing recovery procedures.
- Scaling horizontally to increase aggregate system availability.
- Automatically recovering from failure.

---

## Performance Efficiency

Maintain performance as technologies evolve and demand changes.

### Evaluating includes:

- Experimenting.
- Use serverless architecture.
- Designing systems to go global in minutes.

---

## Cost Optimization

The ability of a system to deliver business value at the lowest price point by:

- Adopting a consumption model.
- Analyzing and attributing expenditure.
- Using managed services to reduce the cost of ownership.

---

## Sustainability

Minimize the environmental impacts of running cloud workloads.

### Key topics:

- Shared responsibility model for sustainability.
- Understanding impact.
- Maximize utilization to minimize resources required and reduce downstream impacts.

---

# AWS PRICING MODELS

## Pay-as-you-go

- Adapt your business based on need, not forecast, reducing the risk of overprovisioning or missing capacity.

---

## Save When You Reserve

- Saving plans for **AWS machine learning, compute and databases** offer savings over **On-Demand** in exchange for a commitment to use a specific amount, measured in **$/hour** of a service or category of service for a **1 or 3-year period**.

---

## Pay Less by Using More

- **Volume-based discounts** for services such as **Amazon S3**.
- Pricing is **tiered**, which means the more you use, the less you pay per **GB**.
Allowing you to integrate legacy systems with cloud  resources 
for example a company might need to keep certain records on premises that can not be moved to the cloud or some legacy systems are better maintained on-site
- **On-premises**: AKA private cloud deployment, in which resources are deployed using virtualization and resource management tools, Increase resource utilization by using application management and virtualization technologies 
---
# AWS GETTING STARTED WITH STORAGE

# INTRO TO STORAGE

- **On-premises storage vs Cloud storage:** On premises refers to when servers exist within the companies infrastructure (on-site), data is transferred through a local network, with cloud storage an outside service such as AWS hosts your data on their infrastructure accessed through the internet.

- **Benefits of cloud storage:**
  - Cost efficient: Pay only for what you use
  - Secure: Data is saved across multiple servers
  - Accessible: Multiple users have access to the storage through IAM (Identity Access Management) user groups, roles and policies.
  - Scalable: Can grow and shrink as workloads grow and shrink.
  - Managed: Dont need to worry about servers and shift focus toward data and applications.
  - Backed up: Copies of data are stored in multiple physical locations in the event of failure.

- **Types of Cloud storage:**
  - Block Storage: breaks data up into blocks and stores them as separate pieces each with own unique indentifier, stored in the most efficient location, each block can be configured to work with different OS
  - File Storage: Helps users, applications and services access data in a shared file system. Stored in a hierarchical structure.
  - Object Storage: Files are stored as objects based on attributes and metadata (object size, purpose etc.). Each object consists of data, metadata and an object key (unique identifier). When updating a file the entire object is updated rather than a piece of a file.

- **Storage use cases:**
  - Block storage: Hosting database instances, Big data analytics and Enterprise applications
  - Object storage use cases: Disaster recovery, Data lakes and Cloud native applications.

- **AWS core storage services:**
  - Amazon Elastic Block Storage (Amazon EBS): A scalable, high-performance block-storage service designed for Amazon Elastic Compute Cloud (EC2), create storage volumes and attach them to EC2 instances
  - Amazon Elastic File System (Amazon EFS): Lets you share file data without provisioning or managing storage
  - Amazon Simple Storage Service (Amazon S3): Stores data as objects (a file and metadata describing that file) within buckets (container for objects).

# INTRODUCTION TO AMAZON SIMPLE STORAGE SERVICE

Amazon S3 is an object level storage service, it stored object within buckets in the region of your choice which are then used in your applications or business operations.

## Use cases

- Data Lakes: for storing large amounts of data
- Websites: file storage for static website hosting
- Backups: for disaster recovery
- Archive: for data that isn't actively used, but should be saved for future use.

## Benefits

- **Scalability:** Designed to grow with the organizations needs, pay only for what you use. Using Amazon S3 automated life cycle rules, you're able to switch between classes to fit your needs.
- **Durability and availability:** Durability describes the average annual expected loss of objects, S3 provides 99.999999999% durability of objects over a given year. Availability is the amount of time per year that an object stored in Amazon S3 is available for retrieval, Amazon S3 provides better than 99.9% availability (almost no down time). SDKs (Software Development Kits) have a configurable retry feature built in, meaning in the case of an availability glitch the SDK will try until it is available.
- **Physical architecture:** When provisioning you choose a region where you want to store your data, when choosing a region objects stored are automatically copied across a minimum of 3 Availability Zones.
- **Protecting and managing files:** Amazon S3 can be configured to replicate data in one region over to another region.

## Security and Compliance

- Employs 3 forms of encryption
- Integrates with AWS CloudTrail for auditing.
- Integrates with Amazon Macie to protect sensitive data.
- Supports security standards and compliance certifications.

## Basic workflow for S3

- Move data into Amazon S3: Accepts data of all file types where individual objects must be below 5 terabytes
- Data gets stored as an object in S3 bucket
- Use Data in Applications: Using an objects unique identifier you're able to use objects across applications.

## Object level storage

- Objects contain:
  - Data: Whats inside the object
  - Metadata: content type, last modified etc
- Key: serving as the objects unique identifier
- Buckets are stored inside a region and objects are stored within a bucket (like a directory or folder in a pc)

- When storing an object in a bucket the combination of the bucket name, key and version ID server as unique identifiers for the object.

## Amazon S3 storage classes

- S3 standard: Most accessed Data the default storage type.
- S3 Standard-Infrequent Access: Accessed less frequently but data must be highly available on request
- S3 One Zone-Infrequent Access: Data accessed less frequently that can be readily recreated if lost.
- S3 Glacier Flexible Retrieval: For archiving data that can be retrieved in a few hours, with expedited retrieval you can retrieve data in 1-5mins.
- S3 Glacier Deep Archive: For archiving data that is not accessed often with a default retrieval time of 12 hours.
- S3 Intelligent Tiering: For unknown or unpredictable data access patterns. Automatically save on storage costs without additional operational overhead or impact on performance.

## S3 class use cases

### Standard

- Static Websites
- Log files frequently accessed, reviewed or analyzed.
- Application installers, configuration files, provisioning and deployment tools.

### Standard-IA

- Backups of systems
- Files that are infrequently accessed but must be readily available if needed.

### One Zone-IA

- Storage for cross-Region replication backups from other buckets.
- Off-site storage of on-premises backups
- Easily replaceable files.

### Glacier Flexible Retrieval

- Long-term backups, archives for compliance or backups that need to be retained for a long amount of time
- Replacement for magnetic tapes stored on-premises or off site.
- Digital media asset archive for large media files.

### Glacier Deep Archive

- Archives or datasets that must be retained for compliance purposes.
- Long term data libraries.

### Intelligent-Tiering

- Unpredictable workloads
- Unknown workloads
- Rapidly changing workloads

## S3 Additional features

- **Lifecycle rules:** Defines a set of actions S3 applies to a group of objects, 2 types; transition actions - define when objects transition from one storage class to another, expiration actions - define when objects expire and are deleted.

- **Replication rules:** offers automatic copying of objects across S3 buckets, can be set up to copy objects to your own or another AWS account, a single bucket, multiple buckets, within the same region or into a different region.

## S3 security

- function under the shared-responsibility model
- By default all buckets are private, you can optionally write an IAM access policy for different users or user groups for controlled access management.
- Another way to grant access is through bucket policies

### Code example

```json
{
  "Version": "2012-10-07",
  "Id": "S3PolicyId1",
  "Statement": [
    {
      "Sid": "IPAllow",
      "Effect": "Deny",
      "Principle": "*",
      "Action": "s3.*",
      "Resource": "arn:aws:s3:::examplebucket/*",
      "Condition": {
        "NotIpAddress": {
          "aws:SourceIp": "54.240.143.0/24"
        }
      }
    }
  ]
}
```

- Encryption: can use either client-side or server-side encryption, CS encryption - for data in transit and at rest, SS - for data at rest

# Moving large amounts of data into Amazon S3

- Transfer acceleration: offers fast straightforward data transfer leveraging Amazon CloudFront globally distributed edge locations.
- AWS snowcone: portable rugged device for edge computing and data transfer, can be used to collect, process and move data to the cloud, comes in HDD and SSD version.
- AWS snowball: uses physical storage devices to transfer large amounts of data between S3 and on-site data storage location at faster-than-internet speeds.
- AWS snowmobile: exabyte-scale data transfer service used to move extremely large amounts of data to AWS, can transfer up to 100 petabytes per snowmobile.

# Additional storage types

## Amazon EBS (Elastic Block Storage)

Amazon EBS (Elastic Block Storage): detachable storage associated with an AZ, when an EC2 instance is stopped data is kept in the EBS volume, can be detached and reattached to different EC2 instances.

- durable, block-level storage device designed for EC2

### Benefits of Amazon EBS

- Data availability: EBS is automatically replicated within its AZ, can be attached to any EC2 in the same AZ,
- Data persistence: is a volume off-instance storage that persists independently of the EC2 instance its attached to, you are charged as long as the data persists. Can be set to automatically detach from an instance with the data intact, and reattached to a new instance for quick data recovery.
- Data encryption: supports encryption. Uses 256-bit Advanced Encryption Standard algorithms (AES-256), and an amazon managed key.
- Data security: Presented to you as raw, unformatted block devices. Amazon EBS service verifies that the devices are logically empty prior to any use or reuse.
- Snapshots: Can be backed up to an S3 by taking point-in-time snapshots
- Flexibility: Can make changes without service interruption, can modify volume type, size and IOPS capacity while in prod.

### EBS volume types

- **SSD:** transactional workloads with frequent read-write operations, and small input output I/O operations per second (IOPS), general purpose - balance of price and performance for most workloads and Provisioned IOPS - high performance for mission-critical, low-latency, or high throughput workloads
- **HDD:** Large streaming workloads that read high throughput performance, throughput optimized HDD- Low-cost HDD for frequently accessed throughput intensive workloads, Cold HDD - lowest cost design for less frequently accessed workloads

## Amazon EFS (Elastic File Storage)

Amazon EFS (Elastic File Storage): Scalable file system used with AWS cloud services and on-premises resources.

- supports thousands of EC2 instances across multiple AZs, accessed through direct-connect.

### Benefits

- Fully managed: AWS handles file service, storage, updating hardware, configuring software and performing backups
- High availability and durability: designed for 99.999999999% durability and 99.99% availability, files are stored across multiple AZs using standard storage classes.
- Elastic and scalable: storage capacity grows and shrinks automatically as you add and remove files.
- Data encryption: Data at rest is encrypted transparently with keys that the AWS Key Management Service manages (AWS KMS). Data in transit s encrypted with industry-standard Transport Layer Security (TLS) to secure network traffic.

### Use cases

- Content management
- Media processing workflows
- Shared home directories
- Database backups
- Dev and application tools
- Big data analytics
---
