# TERMS TO KNOW 





## Test Driven Development 
> is a software development process that relies on the repetition of a very short development cycle: requirements are turned into very specific test cases, then the code is improved so that the tests pass. This is opposed to software development that allows code to be added that is not proven to meet requirements. 

## Continuous Integration 
> Continuous Integration (CI) is a development practice where developers integrate code into a shared repository frequently, preferably several times a day. Each integration can then be verified by an automated build and automated tests. While automated testing is not strictly part of CI it is typically implied. One of the key benefits of integrating regularly is that you can detect errors quickly and locate them more easily. As each change introduced is typically small, pinpointing the specific change that introduced a defect can be done quickly. In recent years CI has become a best practice for software development and is guided by a set of key principles. Among them are revision control, build automation and automated testing. 


## Continuous Delivery
> Continuous Delivery is a software development discipline where you build software in such a way that the software can be released to production at any time.  You’re doing continuous delivery when: your software is deployable throughout its lifecycle Your team prioritizes keeping the software deployable over working on new features. Anybody can get fast, automated feedback on the production readiness of their systems any time somebody makes a change to them. You can perform push-button deployments of any version of the software to any environment on demand

##  Configuration Management 
> Configuration management is a process for maintaining computer systems, servers, and software in a desired, consistent state. It’s a way to make sure that a system performs as it’s expected to as changes are made over time. Managing IT system configurations involves defining a system's desired state—like server configuration—then building and maintaining those systems. Closely related to configuration assessments and drift analyses, configuration management uses both to identify systems to update, reconfigure, or patch.

## Containerization 
> Containerization is defined as a form of operating system virtualization, through which applications are run in isolated user spaces called containers, all using the same shared operating system (OS). A container is essentially a fully packaged and portable computing environment:  Everything an application needs to run – its binaries, libraries, configuration files and dependencies – is encapsulated and isolated in its container. The container itself is abstracted away from the host OS, with only limited access to underlying resources – much like a lightweight virtual machine (VM). As a result, the containerized application can be run on various types of infrastructure—on bare metal, within VMs, and in the cloud—without needing to refactor it for each environment.


## Cloud Scalability, and Reliability 
> Cloud scalability in cloud computing refers to the ability to increase or decrease IT resources as needed to meet changing demand. Scalability is one of the hallmarks of the cloud and the primary driver of its exploding popularity with businesses. 


## Software Architecture 
> Architecture serves as a blueprint for a system. It provides an abstraction to manage the system complexity and establish a communication and coordination mechanism among components. It defines a structured solution to meet all the technical and operational requirements, while optimizing the common quality attributes like performance and security.



## Software Architecture Pattern
> An architectural pattern is a general, reusable solution to a commonly occurring problem in software architecture within a given context. Architectural patterns are similar to software design pattern but have a broader scope. 
      
> Client/Serve - This pattern consists of two parties; a server and multiple clients. The server component will provide services to multiple client components. Clients request services from the server and the server provides relevant services to those clients. Furthermore, the server continues to listen to client requests.

> Peer-to-Peer - In this pattern, individual components are known as peers. Peers may function both as a client, requesting services from other peers, and as a server, providing services to other peers. A peer may act as a client or as a server or as both, and it can change its role dynamically with time.

> Monolithic - In software engineering, a monolithic application describes a single-tiered software application in which the user interface and data access code are combined into a single program from a single platform.

> Microservices  - is a distributed architecture, meaning that all the components within the architecture are fully decoupled from one other and accessed through some sort of remote access protocol (e.g., JMS, AMQP, REST, SOAP, RMI, etc.). The distributed nature of this architecture pattern is how it achieves some of its superior scalability and deployment characteristics.

> Rest - REST, or REpresentational State Transfer, is an architectural style for providing standards between computer systems on the web, making it easier for systems to communicate with each other. REST-compliant systems, often called RESTful systems, are characterized by how they are stateless and separate the concerns of client and server. We will go into what these terms mean and why they are beneficial characteristics for services on the Web.



## CICD PIPE LINE 
### Continous Integration (CI)
> Developers push code to a code repo such as gihub / bit bucket often. a soon a code is pushed a testing(BUILD SERVER) server such as, jenkins CI, checkks the code. this pipline is setup likes this so that the developers can get constant feedback on paased or failed tests. this allows us to find bugs early and fix them. This also allows us the have faster delivery and deploy often.

### Continous Delivery (CD)
> This allows us to ensure that software can be released realiably and often. this proccess allows developers to realse software multiple times every day rather than having a software release every 3 or 4 months apart. usually this proccess is fully automated, it may require a manual step to approve deployment.

### Continous Deployment (CD)
> full automation, every code change is deployed all the way to production, and doesnt require a manual intervention of approval

### Technology stack for CICD 
> Code is pushed to a repo - Build server - testing of code - code is deployed - provisioning  || everythong is managed by aws codepipeline



## Configuration Management

### What is it ?
> Configuration management is a process for maintaining computer systems, servers, and software in a desired, consistent state. It’s a way to make sure that a system performs as it’s expected to as changes are made over time. 

> Managing IT system configurations involves defining a system's desired state—like server configuration—then building and maintaining those systems. Closely related to configuration assessments and drift analyses, configuration management uses both to identify systems to update, reconfigure, or patch.



### Why should you manage configurations?
> Configuration management keeps you from making small or large changes that go undocumented. These misconfigurations can lead to poor performance, inconsistencies, or noncompliance and negatively impact business operations and security. When undocumented changes are made across many systems and applications, it adds to instability and downtime.  

### What tools are used to configure systems?
    * Ansible
    * Cloudformation
    * Terraform 

### Ansible 
> Ansible is a radically simple IT automation engine that automates cloud provisioning, configuration management, application deployment, intra-service orchestration, and many other IT needs. 

> Ansible models your IT infrastructure by describing how all of your systems inter-relate, rather than just managing one system at a time. It's easy to deploy - and most importantly, it uses a very simple language (YAML, in the form of Ansible Playbooks) that allow you to describe your automation jobs in a way that approaches plain English.

### How does Ansible work? 
> In Ansible, there are two categories of computers: the control node and managed nodes. The control node is a computer that runs Ansible. There must be at least one control node, although a backup control node may also exist. A managed node is any device being managed by the control node. 

> Ansible works by connecting to nodes (clients, servers, or whatever you're configuring) on a network, and then sending a small program called an Ansible module to that node. Ansible executes these modules over SSH and removes them when finished. The only requirement for this interaction is that your Ansible control node has login access to the managed nodes. SSH keys are the most common way to provide access, but other forms of authentication are also supported. 


### Cloudformation
> AWS CloudFormation is a service that helps you model and set up your Amazon Web Services resources so that you can spend less time managing those resources and more time focusing on your applications that run in AWS. You create a template that describes all the AWS resources that you want (like Amazon EC2 instances or Amazon RDS DB instances), and AWS CloudFormation takes care of provisioning and configuring those resources for you. You don't need to individually create and configure AWS resources and figure out what's dependent on what; AWS CloudFormation handles all of that. The following scenarios demonstrate how AWS CloudFormation can help.

 ### Why do Developers use Cloudformation ?
 > Developers can deploy and update compute, database, and many other resources in a simple, declarative style that abstracts away the complexity of specific resource APIs. AWS CloudFormation is designed to allow resource lifecycles to be managed repeatably, predictablp, and safely, while allowing for automatic rollbacks, automated state management, and management of resources across accounts and regions.

### How Does AWS CloudFormation work ?
> When you create a stack, AWS CloudFormation makes underlying service calls to AWS to provision and configure your resources. Note that AWS CloudFormation can perform only actions that you have permission to do. For example, to create EC2 instances by using AWS CloudFormation, you need permissions to create instances. You'll need similar permissions to terminate instances when you delete stacks with instances. You use AWS Identity and Access Management (IAM) to manage permissions.

> The calls that AWS CloudFormation makes are all declared by your template. For example, suppose you have a template that describes an EC2 instance with a t1.micro instance type. When you use that template to create a stack, AWS CloudFormation calls the Amazon EC2 create instance API and specifies the instance type as t1.micro. The following diagram summarizes the AWS CloudFormation workflow for creating stacks.


### Terraform
> Terraform by HashiCorp, an AWS Partner Network (APN) Advanced Technology Partner and member of the AWS DevOps Competency, is an “infrastructure as code” tool similar to AWS CloudFormation that allows you to create, update, and version your Amazon Web Services (AWS) infrastructure 

### How does Terraform work ?
> Configuration files describe to Terraform the components needed to run a single application or your entire datacenter. Terraform generates an execution plan describing what it will do to reach the desired state, and then executes it to build the described infrastructure. As the configuration changes, Terraform is able to determine what changed and create incremental execution plans which can be applied.

>The infrastructure Terraform can manage includes low-level components such as compute instances, storage, and networking, as well as high-level components such as DNS entries, SaaS features, etc.


# References 
* https://en.wikipedia.org/wiki/Test-driven_development
* https://codeship.com/continuous-integration-essentials
* https://www.martinfowler.com/bliki/ContinuousDelivery.html
* https://www.redhat.com/en/topics/automation/what-is-configuration-management
* https://www.citrix.com/glossary/what-is-containerization.html
* https://www.vmware.com/topics/glossary/content/cloud-scalability
* https://www.tutorialspoint.com/software_architecture_design/introduction.htm
* https://towardsdatascience.com/10-common-software-architectural-patterns-in-a-nutshell-a0b47a1e9013
* https://en.wikipedia.org/wiki/Monolithic_application#:~:text=In%20software%20engineering%2C%20a%20monolithic,independent%20from%20other%20computing%20applications.
* https://www.oreilly.com/library/view/software-architecture-patterns/9781491971437/ch04.html#:~:text=Basic%20Microservices%20architecture%20pattern&text=The%20microservices%20architecture%20pattern%20addresses,independent%20of%20other%20service%20components.
* https://www.codecademy.com/articles/what-is-rest
* https://www.youtube.com/watch?v=N9KbmHhesmE&feature=youtu.be
* https://www.redhat.com/en/topics/automation/what-is-configuration-management#:~:text=Configuration%20management%20is%20a%20process,changes%20are%20made%20over%20time.
* https://www.ansible.com/overview/how-ansible-works
* https://opensource.com/resources/what-ansible
* https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/Welcome.html
* https://aws.amazon.com/cloudformation/faqs/#:~:text=AWS%20CloudFormation%20is%20a%20service,an%20orderly%20and%20predictable%20fashion.
* https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-whatis-howdoesitwork.html
* https://aws.amazon.com/blogs/apn/terraform-beyond-the-basics-with-aws/#:~:text=Terraform%20by%20HashiCorp%2C%20an%20AWS,Web%20Services%20(AWS)%20infrastructure.
* 