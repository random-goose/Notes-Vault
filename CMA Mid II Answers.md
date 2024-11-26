# APIfication
Creating APIs for software systems, enables seamless communication between different applications and services.

TIMDAMCACI

1. Integration of Services:
	APIs allow different applications, platforms, or services to interact, such as integrating payment gateways, maps or authentication system.
2. Mobile App Development
	Mobile apps rely on APIs to communicate with back-end servers for fetching or sending data, such as social media apps or e-commerce platforms
3. Data Access and Sharing
	APIs facilitate sharing data between systems, often used in open data initiatives, data analytics, and BI tools
4. Automation
	APIs enable process automation, such as automating workflows, data sync, or triggering actions across platforms
5. Microservices
	APIs are the backbone of microservices, allowing individual services to communicate effectively in a distributed system
6. Third Party Integration
	APIs enable external developers to build tools or add-ons for a platform, such as plugins for SaaS products
7.  IoT Applications
	APIs are essential for IoT devices to communicate with servers, applications and other devices
8. Cloud Computing
	Cloud providers use APIs for provisioning resources, managing services, and enabling multi-cloud or hybrid cloud setups
9. AI and Machine Learning
	APIs connect applications of machine learning and AI services such as Natural language Processing, Image recognition etc.
10. Customer Support
	Chatbots, Ticketing Systems, and CRM tools rely on APIs for interacting with customer databases and communication channels


# API Documentation
Creating effecting API Documentation within a Developer Portal is essential for enhancing the developer experience and ensuring seamless integration with your API.
DICEAVGSCC

These are the best practices for creating and maintaining API Documentation
1. Clear and Concise Overview
	1. Provide introduction explaining the APIs purpose, use cases and benefits
	2. Include quick-start guides for new developers to get started easily
2. Detailed API reference
	1. List all the end points, with HTTP methods (GET, POST, etc.) URLs and descriptions
	2. Document request parameters, including required vs. optional fields, data types, and examples
	3. Specify Response Formats (XML, JSON, etc.) along with example responses
3. Interactive API Playground
	1. Offer tools like Swagger UI or Postman Collections for developers to test API calls directly within the portal
	2. Include a sandbox environment for experimentation without affecting live data
4. Code Examples
	1. Provide sample code snippets in multiple programming languages
	2. Ensure examples cover common use cases and also edge cases
5. Error handling
	1. Document all possible error codes and their meanings 
	2. Provide suggestions for resolving common issues
6. Authentication and Security
	1. Explain the auth methods with step-by-step guides
	2. Include security best practices, such as rate limiting and token expiration
7. Versioning Information
	1. Clearly state the API Version and outline how versioning works
	2. Include details about deprecations and migration guides for older versions
8. Glossary and Terminology
	1. Define technical terms and abbreviations to avoid confusion
	2. Provide contextual definitions relevant to your API
9. Search and Navigation
	1. Include a powerful search bar with autocomplete for quick access to documentation
	2. Structure the documentation with a hierarchical table of contents and breadcrumbs
10. Consistent Formatting
	1. Use consistent headers, fonts, and layouts for easy navigation
	2. Utilize visual aids like diagrams, flowcharts, and screenshots to clarify complex processes

# Continuous Deployment v/s Continuous Delivery

| Delivery                                                                                        | Deployment                                                                                   |
| ----------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| Automates the process of preparing code for release but requires manual approval for deployment | Fully automates the process, including deployment to production, without manual intervention |
| Development to production requires manual approval                                              | Deploymnet to production does not require manual approval and is automated                   |
| Suitable for organizations that want more control over production deployments                   | Suitable for organizations aiming for rapid, frequent and automated deployments              |
| Lower risk since human checks are performed before deploying to production                      | Higher risk since code is automatically deployed to production                               |
| Slower feedback loop as deployment is slower and a manual process                               | Fast feedback loop due to full automation, and faster deployments                            |
CD Tools:
1. Jenkins
2. GitLab CI/CD
3. CircleCI
4. Azure DevOps
5. Travis CI
6. Team City

# Advantages and Challenges of Microservices

### Advantages
- Scalability
	- Individual services can be scaled independently, optimizing resource usage and improving performance
- Faster Deployment and Development
	- Teams can work on separate services independently, which parallelizes the development and deployment process
- Fault Isolation
	- Failures in one service are less likely to affect the whole system, improving reliability and uptime
- Technology Flexibility
	- Teams can use different programming languages, runtime environments, frameworks allowing for better DX
- Easier Maintenance and Updates
	- Services and be updates or replaced without affecting other parts of the application, ensuring smoother upgrades

### Challenges
- Complexity in Management
	- Managing multiple services, dependencies, and communication between them increases system complexity
- Inter-Service Communication
	- Requires robust protocols like REST APIs to handle services
- Increased Deployment Overhead
	- Coordinating deployments of multiple services can be complex, especially when services depend on each other
- Monitoring and Debugging
	- Identifying issues across multiple service is more difficult and requires advanced monitoring tools
- Testing Difficulties
	- End-to-End testing becomes challenging due to the distributed nature of microservices

# Blue-Green v/s Canary

| Blue-Green                                                                                                                 | Canary                                                                                                    |
| -------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| Two environments, blue and green are maintained. Traffic switches between the old (blue) to the new (green) once validated | Gradual rollout of the new version to a subset of users, incrementally increasing until the full roll out |
| Immediate Rollouw                                                                                                          | Gradual and controlled rollout                                                                            |
| Easy Rollback                                                                                                              | Complex rollback                                                                                          |
| High resource usage as two full environments run simultanenously during the development                                    | Moderate usage as resources scale incrementally with rollout progress                                     |
| Entire traffic switches between the two environments via a load balancer                                                   | Traffic is split dynamically via trafficc rules                                                           |
| Standard monitoring before and after deployment                                                                            | Requires detailed monitoring to analyze user impact at each stage                                         |
| Best for deployments with critical changes or when downtime is acceptable                                                  | Best for high-rick deployments needing user feedback and uptime                                           |

# Serverless
It is a cloud-based architecture where the cloud provider manages the infrastructure, allowing developers to focus solely on writing code. Applications run in stateless, ephemeral containers, and resources are automatically allocated based on demand.

Characters:
- No server management
- Event driven execution
- Pay-per-use pricing

**Scenario:** High-Volume Image Processing Platform
- Reasons:
	- Automatic Scaling
	- Cost Efficiency
	- Event Driven Architecture
	- Reduced Operational Complexity


# Try Catch Python
This is used doe exception handling, enabling programs to handle errors gracefully without crashing. It separates normal code execution from error-handling logic, making programs more robust and user-friendly.

### How it works:
1. **Try**
	1.  Contains code that might raise an exception
	2.  If no exception occurs, the try block gets executed and skips the except block
2. **Except**
	1. Catches and handles specific exceptions raised in the try block
	2. Prevents the program from crashing
3. **Else**
	1. Runs the code if no exceptions were found in the try block
4. **Finally**
	1. Executes this block of the code regardless of whether an exception arose or no

### Use in Error handling
- Graceful Error Recovery
- Custom Error Handling
- Debugging Assistance
- Code Clarity
- Resource Management

```python
try:
	x = numerator / denominator
except ZeroDivisionError:
	print("0 division error")
else:
	print(f"result = {x}")
finally:
	print("Division completed")
```

