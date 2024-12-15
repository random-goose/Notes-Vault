# Unit I
### Cloud Service Components
are the building blocks of cloud computing, enabling the delivery of computing services over the internet. There are three main service components:
- **Infrastructure as a Service IaaS**: Provides a virtual data center to store information and create platforms for app development, testing, and development. It allows users to access resources such as virtual compute resources and virtual storage
- **Software as a Service**: Provides web software and apps to complete business tasks. It is a software in which the apps are hosted by a cloud provider, and users can access these applications with the help of a browser and an internet connection
- **Platform as a Service**: Provides a runtime environment
- **Serverless**: A cloud service model where the cloud provider dynamically allocates and charges for the resources consumed for every execution of the code.

### Cloud Service / Deployment Models
are virtual computing environments with development architectures that vary depending upon the amount of data you store and who needs access to the data
- **Public Cloud**: This allows anyone to access systems and services. It is less secure as it is open to everyone
- **Private Cloud**: This is a one-on-one environment for a single suer or customer. There is no need to share your data with anyone else
- **Hybrid Cloud**: This combines the public and private worlds with a layer of proprietary software
- **Community Cloud**: This allows systems and services to be accessible by a group of organizations.

### Applications of Cloud Computation
- Art-Related Applications
- Image-Editing
- Data-Storage
- Business Applications
- Education
- Big Data Analytics
- Testing
- Entertainment
- E-Commerce 
- Social Media
- Antivirus
- Firewall

# Unit II
### Public Cloud Platforms
is a cloud computing architecture where a cloud service provider makes cloud resource like processing capacity, storage, and applications accessible to the public via the internet. Users can access these resources on a pay-per-use basis, and they are shared among many users.
Public cloud platforms are used by organizations to access and use cloud resources without having to manage the underlying infrastructure themselves.
- Amazon Web Services
- Microsoft Azure
- Google Cloud Platform
- IBM Cloud
- Oracle Cloud Infrastructure
- Alibaba Cloud

### Monolithic v/s Distributed

#### Monolithic
 A traditional software design model where all application components are integrated into a single, self-contained unit.
Components:
- User Interface
- Business Logic
- Data Access
- Database

Advantages:
- Easy to develop and deploy
- Simplified Testing and Debugging
- Performance
- Centralized & Management
- Easy Debugging

Disadvantages:
- Scalability Issues
- Tight Coupling
- Update Challenges
- Limited Agility
- Limited Fault Tolerance

#### Distributed
often implemented using microservices, dividing an application into smaller loosely coupled services. Each service typically runs in its own process and communicates via APIs or messaging queues.

Advantages:
- Scalability
- Fault Isolation
- Flexibility in Tech Stack
- Faster Development Cycles
- Adaptable and Agile

Disadvantages
- Complexity
- Latency and Performance Bottlenecks
- Operational Overhead
- Data Consistency

Monolithic is more suited for low complexity applications made by a small team or when speed of development is a priority
Distributed Architecture is ideal for large scale applications with high demands for scalability, resilience, and agility - often used for cloud native apps

### 12 Factor App
is a methodology used for building SaaS Applications that are designed to run in the cloud. It provides a set of best practices and guidelines for develping cloud-native apps, ensuring scalability, resliency, and ease of management

CDC BB PPC DLLA

Codebase
Dependencies
Config
Backing Services
Build Release Run
Processes
Port Binding
Concurrency
Disposability
Dev/Prod Parity
Logs
Admin Processes

### Microservices
it is a software design approach that structures an application as a collection of small, independent services. Each service focuses on a specific business capability and communicates with others through well-defined APIs.

Design Principles:
- Single Responsibility
- Open-Closed Principle
- Liskov Substitution Principle
- Interface Segregation
- Dependency Inversion

Challenges:
- Distributed Complexity
- API Design
- Data Management
- Testing and Debugging
- Security

# Unit III
### API Tools
Development - Postman: Telisinde
Testing - SoapUI: Soap ante serial - serials patience ni test chestai
API Monitoring - Pingdom: Monitoring ante pinging cheyyali anduke Pingdom
Documentation - Swagger: Documentation should be dripped out as fuck so swagger
API Management - Kong: Manager = king; king - kong

### Apification
is the process of exposing functionalities and data as APIs, which has revolutionized how businesses operate and interact with their customers, partners, and internally. 
Applications:
- Digital Transformation
	- Modernizing Legacy systems
	- Creating new digital products
- Business Process Automation
	- Automating Routines
	- Orchestration Complex Workflows
- Data Integration and Sharing
	- Consolidating Data Silos
	- Sharing Data with Partners and Customers
- Enhancing Customer Experiences
	- Personalization
	- Omnichannel Integration
- Enabling Innovation and Partnerships
	- Developer Ecosystems
	- Strategic Partnerships

Specific Use Cases 
- Financial Services
	- Open Banking
	- Payment Processing
	- Fraud Detection
- Healthcare
	- Electronic Health Records
	- Telehealth
	- Clinical Trials
- Retail
	- Inventory Management
	- E-Commerce
	- Loyalty Programs
- Manufacturing
	- Supply Chain Management
	- IoT Integration

### Cloud Security and Monitoring Tools
are essential for ensuring the safety and performance of cloud-based systems and applications.
- IAM - Identity and Access Management - AWS IAM, Azure Active Directory
- Data Encryption - AWS, Google Key Manager Service (KMS)
- Cloud Monitoring - Grafana


