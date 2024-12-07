# Unit I
### Website: Uses and Purpose
A website is a collection of related web pages hosted on the internet, accessible via a unique domain name.
It serves as a platform for sharing information, communication, commerce, and interaction.

Need:
- Accessibility - Provides a globally available 24/7 access to information and services
- Cost-Effectiveness - Reduces the need for physical infrastructure
- Convenience - Streamlines communication and transactions for users

Purpose:
- Information Sharing - Disseminates knowledge, updates, and guidance
- Business Growth - Facilitates marketing, customer engagement, and sales
- Brand Presence - enhances visibility, and credibility of organizations or individuals 
- Interaction - Enables user engagement through tools like forms, chat or e-commerce


### Static and Dynamic Websites
#### Static
They consist of fixed content delivered to users exactly the way it is stored. The pages are pre-rendered and do not change unless manually updates by a developer.

Characteristics:
- Built using basic web technologies like HTML, CSS, and optional JavaScript for minor interactivity
- Each page is a separate file stored on the server, and there is no database involved.
- Best suited for smaller websites such as personal portfolios, informational sites, or company profiles with minimal updates
Advantages
- Fast Loading - because the pages are pre-rendered and there is no reliance on databases or backend, pages load quickly
- Cost Effective - Simple to develop, host, and maintain
- High Security - without any backend interaction, they are inherently secure
Disadvantages
- Static Content - content remains the same unless manually updated
- Scalability Issues - Not ideal for websites that require frequent updates or user interaction
- Limited functionality - Cannot handle complex tasks

#### Dynamic
generate content in real-time base don user interactions, external data, or backend logic. The content changes dynamically, making these websites more interactive and versatile

Characteristics
- Built using server-side scripting using languages and frameworks like python - Django, JavaScript - Node, or PHP
- Typically connected to a database to store and retrieve information
- Used for complex applications like e-commerce platforms, social media sites, or blogs with frequent updates and interactivity are essential
Advantages
- Interactive Content - Provides a personalized experience for users by tailoring content based on their actions or preferences
- Easy Updates - using Content Management Systems (CMS) like WordPress allow non-technical suers to update content effortlessly
- Advances Features - Supports functionality like authentication, data processing, and e-commerce
Disadvantages
- Higher Deployment Costs
- Slower Loading times
	- Database Queries
	- Server-side rendering
- Increased Security Risks - More Vulnerable

### HTML
Hyper Text Markup Language is a standard markup language used to create and design web pages
It structures content on the web, defining elements like text, images, links, and multimedia
- Uses predefined tags
- Focuses on visual presentation and user interaction
- Supports links to navigate across web pages
- Creating the structures of websites
- Designing forms, tables, and multimedia content

### XML
extensible Markup Language is a markup language designed to store and transport data in a structure and readable format
Focuses on data storage and exchange rather than presentation
- Customizable tags - allows users to create own tags
- Hierarchical Structure - trees
- Platform-independent
- Data exchange between applications
- Configuration files

### JSON
JavaScript Object Notation is a lightweight data-interchange format that is easy for humans to read and write and for machines to parse and generate
Is primarily used for transmitting data between a server and a web app
- Simplicity - key:value
- Lightweight
- Language-Independent
- APIs for data exchange
- Storing configuration and state info

| Feature         | HTML                  | XML                     | JSON                     |
| --------------- | --------------------- | ----------------------- | ------------------------ |
| **Purpose**     | Web content structure | Data storage & exchange | Data transmission        |
| **Format**      | Predefined tags       | Customizable tags       | Key-value pairs          |
| **Readability** | Human-readable        | Human-readable          | Highly human-readable    |
| **Usage**       | Website design        | Inter-application data  | APIs and web development |
