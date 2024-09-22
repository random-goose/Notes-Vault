![[Screenshot 2024-09-21 133442[1].png]]
![[cloud  imp set 2[1].jpg]]

# 1
## Cloud Computing
It is the delivery of computing resources such as compute (CPU or GPU or TPU etc.), Storage, Databases, Networking, Software and Analytics - over the interned. It allows the users to access and store data on remote servers rather than devices on premises, which in theory provides flexibility, scalability, and savings

- On Demand: Users can provision computing resources as needed without using human intervention
- Broad Network access: servers can be accesses form anywhere via the internet
- Resource Pooling: Provides users with shared resources
- Scalable: Resources can be scaled up or down based on demand
- Measured: Cloud systems monitor and report the usage, allowing for cost optimization

### Applications
- Data Storage - Dropbox, Google, Amazon s3
- Saas - Microsoft 365, Salesforce, Slack
- Web Hosting - AWS, Google Firebase, Vercel
- Streaming Services - Netflix, YouTube, Spotify
- AI and ML: Google AI, IBM Watson, OpenAI
- Data Analytics: Amazon Redshift, Google BigQuery

### Services
- IaaS - AWS
- Platform aaS - Heroku
- SaaS - Adobe
- Storage aaS - S3
- DB aaS - Mongo Atlas
- Functions aaS - Serverless Computing - Vercel
- AI aaS - IBM Watson
- Comm aaS - Slack
- CDN
- Monitoring of Resources

### Advantages
- Cost Effective (theoretically)
- Scalability
- Accessibility
- Automatic Updates
- Disaster Recovery
### Disadvantages
- Internet Dependency
- Security Concerns
- Limited Control
- Vendor Lock-In
- Potential Downtime
- Compliance Issues

#### Utilization Management
- Resource Monitoring
- Auto-Scaling
- Load Balancing
- Performance Optimization
- Cost Management

### Security
- Access Control
- Encryption
- Network Security
- Compliance
- Regular Audits
- Incident Response

## Mobile Computing
refers to the use of portable computers such as laptops, tablets, smartphones and wearables, which allow the user to perform computational tasks anytime and anywhere, typically over a wireless network, either 4g/5g mobile networks or Wi-Fi. It allows seamless access to applications, internet services and data storage when on the move
- Use of Mobile Hardware
- Different software tailored to the mobile devices
- Communication Networks
- Portability
- Real Time Access
- Increased Productivity
- Mobile Banking - Pay TM, Google Pay
- GPS Navigation
- Social Media
- Healthcare
- Gaming

# Monolithic v/s Microservices

## Monolithic - Amazon
it's the architecture where the entire application is built as a single unit or a single tier system. All functions - UI, business logic, and database layers - are tightly integrated and managed within one codebase.
- Single Large Codebase
- Tightly coupled components
- Difficult to scale and maintain
- East to develop but hard to update

## Distributed - Netflix
in this architecture, the application is split into multiple components or services that communicate with each other over a network. Each component is individually developed, deployed and scaled.
- Distributed codebase
- Loosely coupled components
- Easier to update and maintain
- more resilient as multiple points of failure are present
- harder to develop initially but easier to update and maintain


# 12 Factors
- Codebase - One codebase tracked + many deploys
- Dependencies - Declare + Isolate dependencies
- Config - Store config in Environment
- Backing Services - Treat backing services as attached resources
- Build  Release  Run - Strictly separate build and run stages
- Processes - Execute the app as one or more stateless processes
- Port Binding - Export services via port binding
- Concurrency - Scale out via process model
- Disposability - Maximize robustness
- Dev/Prod Parity - Keep dev/staging/prod as similar as possible
- Logs - treat them as event streams
- Admin Processes - run them as a one-off process