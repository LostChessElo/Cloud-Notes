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
