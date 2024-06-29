# Cloud

## private cloud

- A Private Cloud Infrastructure is implemented by a company using its own hardware. The specific computer hardware needs to be purchased, implemented, and maintained by the company.
- The computer hardware that needs to be procured by a company will typically consist of several components, including servers, switches, and routers. This may have a massive financial impact on the company.
- Hardware can be situated locally on the company premise or in a Datacenter of a third-party provider.
- A Private Cloud is used to create a pool of computer resources that can then be accessed and utilized by the company.
- Different types of Private Cloud software are available from different vendors, including Microsoft, Red Hat, and Suse. This software is designed to implement a private cloud infrastructure and provide the needed services to access the resources allocated to it.

## Public cloud

- With a Public Cloud Infrastructure, the computer resources are procured, implemented, and maintained by a third-party provider, for example, Microsoft. The computing hardware is situated in Datacenters across the world and is accessible through the internet, and can be accessed by anybody who has purchased these specific services or resources.
- The resources that are provided include computing, networking, and storage.
- Specific cloud services are provided, which can then utilized by companies for specific purposes. Companies that access these services pay for the computing resources being utilized but do not need to maintain the back-end hardware.

## Hybrid cloud

- A Hybrid Cloud Infrastructure is a combination of a public and private cloud where the services that are provided are shared between the different infrastructures. The public and private infrastructures are connected to each other through the internet to ensure the available resources.
- This type of cloud infrastructure is used when the demand for resources fluctuates, and the Private Cloud cannot meet these demands. The Public Cloud’s Infrastructure is then used to seamlessly scale the resources to meet these demands.

## Community cloud

- A Community Cloud infrastructure refers to shared cloud computing resources that are shared between a set of organizations with the same business goals, for example, Universities or Colleges. These organizations have the same or similar security, privacy, and resource utilization concerns. These cloud infrastructures may be managed by a single organization or a third-party provider and can be hosted on-premise or in a data center, depending on the needs of the community. The data that is shared on a Community Cloud is available to all the participants of the community cloud infrastructure.

## different cloud services

Infrastructure as a Service (IaaS):

- Infrastructure as a Service (IaaS) cloud service provides specific computing resources using either a Public or Private Cloud Infrastructure. These computing resources include providing virtual machines that will be accessible through the internet using remote accessing protocols, for example, Remote Desktop (RDP) or a Secure Shell (SSH).
- By provisioning these resources, it will be the customers' responsibility to maintain these resources' software and operating systems. The hardware these resources utilize, for example, hard drives and computing, will be maintained by the Cloud Provider.
- The benefit of using Infrastructure as a Service (IaaS) is that the customer will not need to incur any hardware costs to create a specific computing resource. Another benefit is if more resources for a particular computing resource are needed, it can be easily provisioned with little or no downtime depending on the resource that needs to be added.

Platform as a Service (PaaS):

- Platform as a Service (PaaS) in Cloud computing refers to the concept that a specific application or service is used without the necessity of creating a complex backend infrastructure. An example of PaaS is creating a SQL database. The customer would create the database on the Cloud Service providers platform, for example, the Azure Web portal. There will be no need to create a server to host the database; this is done by Azure in the backend and hosts the SQL Database for the customer. The customer will still need to maintain the application but not the backend servers which host the application.
- The benefit of using Platform as a Service is the customer does not need to maintain the server infrastructure that will be hosting the application. Thus the overhead costs for management are less. There will be no licensing and hardware costs. Hence the organization tends to save more.

Software as a Service (SaaS):

- In a Software as a Service cloud service, the application which will be used by the customer is managed and maintained by the Cloud Service Provider. The customer has little to no interaction with maintaining the application in the backend. An example of Software as a Service application is Microsoft 365.
- Microsoft 365, previously known as Microsoft Office 365, includes a suite of cloud applications for end-users. The following is a list of some of the applications available in Microsoft 365:
- Exchange Online: An online email application hosted by Microsoft. This application replaces the traditional on-premises Exchange server reducing the amount of hardware needed to host the on-premise server.
- Teams: Formerly known as Skype for Business Online, it is an online communication and collaboration tool which can be used for internal and external communication using instant messaging, voice, and video calling.
- SharePoint Online: A company can provide a SharePoint Online service without having a physical server to host the application. In Microsoft 365, this an online application with all the features and functionality of an on-premise SharePoint server, thus reducing the company's hardware footprint.

Desktop as a Service (DaaS):

- Desktop as a Service (DaaS), a Virtual Desktop Infrastructure (VDI), is provided and maintained by a third-party provider, for example, a Cloud Service Provider like Microsoft Azure.
- The difference between hosting a Virtual Desktop Infrastructure and accessing it through a CSP is that the CSP will manage and maintain the backend of the VDI.
- A Desktop as a Service defines a Desktop operating system. For example, Windows 10 runs as a virtual machine on a server of the Cloud Service Provider.
- The customer will access these devices and maintain the software, and the CSP will maintain the storage, backup and security of these virtual devices. Depending on the type of service plan agreed with the CSP, the customer will also maintain the security of the virtual device's applications.

Infrastructure as Code:

- Infrastructure as Code (IaC) is used to generate the same virtual infrastructure (Virtual networks, load balancers and connection topology) every time, which can then be collectively managed using the code. DevOps teams can use IaC to test applications in environments replicating the production environment closely.

## cloud connectivity options

- Resources that are created on a Cloud Service provider need to be accessed by the customer securely. Different cloud connectivity options are available when connecting to these resources. The different Cloud Service providers provide several different ways of connecting to resources in the cloud.

Virtual Private Network (VPN):

- Cloud resources that have been created on a Cloud Service Providers infrastructure need to be accessed securely. A virtual private network can be created between the Cloud Service Provider’s infrastructure in the customer's on-premise infrastructure. Depending on the Cloud Service Provider, the way of creating and connecting using a VPN connection may vary.

Virtual Private Network (VPN):

- Cloud resources that have been created on a Cloud Service Providers infrastructure need to be accessed securely. A virtual private network can be created between the Cloud Service Provider’s infrastructure in the customer's on-premise infrastructure. Depending on the Cloud Service Provider, the way of creating and connecting using a VPN connection may vary.

Cloud Multitenancy:

- In Cloud computing, the term multitenancy refers to the concept of where several different users share the resources provided by the Cloud Service provider. The resources that are utilized are allocated to specific users, ensuring that the users won’t be able to access each other data. Cloud multitenancy can be applied to be used by Public and Private Cloud providers.
- The benefits of using multitenancy are that it will reduce the cost of the resources being utilized, and the resources will be used to their full extent.

## Security Implications using Cloud Services

- Several security considerations need to be taken into account when considering a Cloud Service Provider to host-specific resources in the cloud.

The following are some of the security aspects that need to be considered:

Data Security - The Cloud Service provider needs to provide proof that the data stored in the cloud will be safe and not accessible to other parties.
Resource Availability - A Service Leval Agreement (SLA) needs to be provided by the Cloud Provider, ensuring resource availability for all customers.
Software connection interface - Most software applications use an Application Programming Interface (API) to ensure connectivity. Security risk can occur if these API’s are not secure. A Cloud provider needs to ensure that data encryption and transport security protocols are applied to these API’s to prevent a breach in security.
The data's location - A Cloud Provider needs to provide in which country and region the client's data are stored to ensure compliance to data regulations of different countries. In the United Kingdom, data compliance is regulated by the GDPR act. Different countries will have different policies to ensure data compliance.
