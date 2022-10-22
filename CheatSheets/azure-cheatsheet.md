---
title: Microsoft Azure Fundamentals Cheatsheet
description: Azure cheatsheet contains important concepts while working with azure.
created: 2022-10-14
updated: 2022-10-14
---
Azure Fundamentals consist  of cloud concepts, Azure services, Azure workloads, security and privacy in Azure, as well as Azure pricing and support.

## Basics
Cloud computing has started to evolve as one of the pillars of the new normal during the global pandemic. Amongst all the major players,like google cloud , amazon cloud  Microsoft Azure is becomming  one of the leading choices of enterprises worldwide. 

## Azure Cloud Concepts
## 1. Benifits of Cloud Computing
Cost-effective solutions
Easy accessibility from anywhere
Faster Deployments of typically large environments

### 2. Cloud Models
The cloud models define the deployment type of cloud resources. The three main cloud models are: 
## private, public, and hybrid.

 ### 2.1. Private Cloud 
 It’s a cloud  that’s used by a single entity(where security is main concern). Private cloud provides much greater control for the company and its IT department. However, it also comes with 'greater cost' and 'fewer'  of the benefits of a public cloud deployment

 ### 2.2. Public cloud 
 A public cloud is built, controlled, and maintained by a third-party cloud provider. With a public cloud, anyone that wants to purchase cloud services can access and use resources. 
 Typical examples of public cloud are 
 ## -Google , Aws , Azure

 ### 2.3. Hybrid Cloud
 A hybrid cloud is a computing environment that uses both public and private clouds in an inter-connected environment. A hybrid cloud environment can be used to allow a private cloud to surge for increased, temporary demand by deploying public cloud resources.
 It can be used to provide an extra layer of security. For example, users can flexibly choose which services to keep in public cloud and which to deploy to their private cloud infrastructure.

 ## 3. Cloud Models
 ### 3.1 Shared Responsibility Model 
 shared responsibility model, these responsibilities get shared between the cloud provider and the consumer. Physical security, power, cooling, and network connectivity are the responsibility of the cloud provider. Responsibilities are shared between Cloud Provider and consumer based on Azure offerings(Saas , Paas , Iaas).
 For Onpremise offering everything is responsibility of customer.

 ### 3.2 Consumption Based Model
 In IT infrastructure models, there are two types of expenses to consider. First being Capital expenditure (CapEx) and  second operational expenditure (OpEx).
○ CapEx is typically a one-time, up-front expenditure to purchase or secure tangible resources
○ OpEx is spending money on services or products over time. 

### 4 Examples of Consumption Based Model (Cap-Ex & Op-Ex)
 ### Cap-Ex 
  Buying new building, repaving the parking lot, building a datacenter, or buying a company vehicle.
 ### Op-Ex 
  leasing a company vehicle, or signing up for cloud services .

 ## 5 .Cloud Services( Iaas , Paas , Saas)
### Infrastructure as a service(Iaas)- 
It is most flexible category of cloud services, as it provides you the maximum amount of control for your cloud resources. In an IaaS model, the cloud provider is responsible for -  maintaining the hardware, network connectivity (to the internet), and physical security. You’re responsible for - operating system installation, configuration, and maintenance; network configuration; database and storage configuration;

### 5.1  Platform as a service (PaaS)-
 is a middle ground between renting space in a datacenter (infrastructure as a service) and paying for a complete and deployed solution (software as a service). In a PaaS environment, the cloud provider maintains - physical infrastructure, physical security, and connection to the internet.
 PaaS scenario, you don't have to worry about the licensing or patching for operating systems and databases.
 PaaS is  suited to provide a complete development environment without the headache of maintaining all the development infrastructure.

 ### 5.2 Software as a service (SaaS)-
  is the most complete cloud service model from a product perspective. With 'SaaS', you are essentially renting or using a fully developed application. Financial software, messaging applications, Email  and connectivity of  software are examples under category of Saas offering.

## 5.3 Benifits of Managment in Cloud 
*Automatically scale resource deployment as per need.*
*Monitor the health of resources and automatically replace failing resources.*
*Receive automatic alerts based on configured metrics .*

## 6. Scaling In Cloud 
When building or deploying a cloud application, two of the biggest considerations are uptime (or availability) and the ability to handle demand (scale)

### *Types Of Scaling*
### Horizontal Scaling
### Vertical Scaling

## Horizontal Scaling - 
 In horizontal scaling, if you suddenly experienced a steep jump in demand, your deployed resources could be scaled out (either automatically or manually). This can be done by add additional virtual machines or containers, scaling out.

 ## Vertical Scaling  -
 you could vertically scale up to add more CPUs or RAM to the virtual machine & also  you could vertically scale down by lowering the CPU or RAM specifications.

 ### 7.Azure Accounts - 
 To create and use Azure services, you need an Azure subscription
 When you're working with your own applications and business needs, you need to create an Azure account, and a subscription will be created for you.

 ### 7.1 Azure Free Account includes:

Free access to popular Azure products for 12 months.
A credit to use for the first 30 days.
Access to more than 25 products that are always free. 

### 7.2 Azure Student Account
Free access to certain Azure services for 12 months.
A credit to use in the first 12 months.
Free access to certain software developer tools.

## 8 . Steps to Create Azure Resources
### create a virtual Machine
1.  Sign in to the Azure portal.
2.  Select Create a resource > Compute > Virtual Machine > Create.
3.  The Create a virtual machine pane opens to the basics tab.
4. Verify or enter the following values for each setting. If a setting isn’t specified, leave the default value.
| Setting            | value                     |
| -----------         |---------                 |  
|Subscription        | Concierge Subscription    |
| Resource group     | Resource group            | 
| Username           |  azureuser                |
Public inbound ports | None                      |

5. Select Review and Create.


###  9 .Azure Compute & Networking Services.
## 9.1 Azure Virtual Machines -
Azure Virtual Machines (VMs), you can create and use VMs in the cloud. VMs provide infrastructure as a service (IaaS) in the form of a virtualized server and can be used in many ways. 
Vm can be helpfull when 
**Total control over the operating system (OS).**
**The ability to run custom software.**
**To use custom hosting configurations.**
## 9.2  Virtual Machine scale set
Scale sets allow you to centrally manage, configure, and update a large number of VMs in minutes. The number of VM instances can automatically increase or decrease in response to demand, or you can set it to scale based on a defined schedule.
Helpfull in building  large-scale services for areas such as compute, big data, and container workloads.
## 9.3  Virtual availability sets 
availability sets are another tool to help you build a more resilient, highly available environment. Availability sets are designed to ensure that VMs stagger updates and have varied power and network connectivity, preventing you from losing all your VMs with a single network or power failure.


## 10 .Examples when to use Virtual Machines.
During testing and development
When extending your datacenter to the cloud
During disaster recovery:

## 11.Azure Functions
Azure Functions is an event-driven, serverless compute option that doesn’t require maintaining virtual machines or containers. 

## 12. Azure Virtual Private Networks
A virtual private network (VPN) uses an encrypted tunnel within another network. VPNs are typically deployed to connect two or more trusted private networks to one another over an untrusted network . Traffic is encrypted while traveling over the untrusted network to prevent eavesdropping or other attacks.

## 13.Virtual Private Network Gateways
A VPN gateway is a type of virtual network gateway.
*Connect on-premises datacenters to virtual networks through a site-to-site connection. *
* Connect virtual networks to other virtual networks through a network-to-network connection.*

## 14 .VPN Gateway is usefull in folllowing cases-
*Connections between virtual networks*
*Point-to-site connections*
*Multisite connections*

## 15. Azure DNS
Azure DNS is a hosting service for DNS domains that provides name resolution by using Microsoft Azure infrastructure
## Benifits of Azure DNS 
*Security*
*Customizable virtual networks*
*Alias records*

### Azure Storage Services.
## *Azure Blobs*
## *Azure Files*
## *Azure Queues*
## *Azure Disks*

## 16. Benifits of Azure Services
Durable and highly available
Secure
Managed
Accessible 

## Links to Resources 
https://learn.microsoft.com/en-us/certifications/azure-fundamentals/
https://azure.microsoft.com/en-in/free/


```


