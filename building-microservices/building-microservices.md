# Building Microservices

## 1. Microservices
<br>

### What Are Microservices?

#### Small, and Focused on Doing One Thing Well
- small enough and no smaller -- once a piece of code no longer feels to big, it's probably small enough
- the smaller the service, the more you maximize the benefits and downsides of microservices

#### Autonomous
- all communication between services are via network calls to enforce seperation and avoid tight coupling
- need to be able to change independently of each other
- deployed by themselves without requiring consumers to change
- golden rule: **can you make a change to a service and deploy it by itself without changing anything else?**

<br>

### Key Benefits

#### Technology Heterongeneity
- can decide to use a different technology stack for each service
- "pick the right tool for each job"
- able to adopt technology more quickly
    - pick a service with the lowest risk/potential impact and use the new technology there

#### Resilience
- build systems that handle the total failure of services and degrade functionality accordingly
- need to understand the new sources of failure that distributed systems have to deal with

#### Scaling
- with a monolithic service we have to scale everything together
- with smaller services, we can just scale those services that need scaling
- allows us to control our costs more effectively

#### Ease of Deployment
- with microservices we can make a change to a single service and deploy it independently of the rest of the system
- if a problem occurs, it can be isolated quickly

#### Organizational Alignment
- smaller teams working on smaller codebases tend to be more productive

#### Composability
- opens up opportunities for reuse of functionality
- microservices alow for our functionality to be consumed in different ways for different purposes

#### Optimizing for Replaceability
- the barriers to rewriting or removing services entirely are very low
- teams using microservices are comfortable with completely rewriting services when required, and killing a service when it is no longer needed

<br>

### What About Service-Oriented Architecture?
- SOA is a design approach where multiple services collaborate to provide some end set of capabilities
- despite many efforts there is a lack of good consensus of how to do SOA well
- many of the problems with SOA are actually problems with things like communication protocols (ex. SOAP), vendor middleware, a lack of guidance about service granularity, or picking where to split a system
- microservices are a specific approach for SOA in the same way Scrum is a specific Agile approach

<br>

### Other Decompositional Techniques

#### Shared Libraries
- provide reuse between teams and services
- lose true technology heterogeneity: typicall has to be in the same language/platform
- scaling parts of your system independently is lost

#### Modules
- technically it should be possible to create well-factored independent modules within a single monolithic process
    - in practice we rarely see this happen
- become tightly coupled with rest of the code, surrending their key benefits

<br>

### No Silver Bullet
- microservices are no silver bullet