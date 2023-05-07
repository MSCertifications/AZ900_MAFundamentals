# AZ-900 Microsoft Azure Fundamentals

## Azure Portal

The most approachable way to interact with Azure. It's used to build, manage and monitor everything from simple web apps to complex cloud applications in a single, unified console.

### Features

**Personalize**
- Create our own dashboards, layouts, workflows and colors.

**Access Control**
- Fine-grained access control to all our resources. This will make management and governance much easier.

**Const Management**
- Great tooling to keep track of current and projected spend for our Azure resources.

### Azure CLI

- Stable.
- Structure: CLI commands are structured very logically adn all follow the same pattern.
- Cross platform
- Automation: It is simple automate the CLI command for future use.
- Logging

### Azure PowerShell

- Cmdlet: A script that performs a specific task. "New-AzVM" creates a new Virtual Machine.
- Azure Resource Manager: PowerShell also uses the Resource Manager, like the Portal, to manipulate Azure resources.

### Cloud Shell

It is an interactive, browser-accessible shell for managing Azure resources.

### ARM (Azure Resource Manager) templates

- It's the gatekeeper to managing anything in Azure. They are a way to describe which resource we want to create, delete, manage, alter, or do any number of actions to.
- It's declarative: specify **what** we want, not **how** it is done.
- It's a common language and syntax that could be used for idempotent actions.
- No human errors.

### Azure Advisor

It provides recommendation to improve availability of resources, save costs on services, increase reliability, and so on.

# CHAPTER 02 - CLOUD CONCEPTS

Cloud computing is the on-demand availability of computer system resources split into three main categories:

* Compute
* Networking
* Storage

The main benefits are:

* Low cost
* Ease of adption
* Almost unlimited resources

## The language of cloud computing

**High availability**

It's core to the cloud.

* We dont' own the HW.
* Add more servers with a click.
* If HW fails, replace it instantly.
* Use clusters to ensure high availability.

**Reliability**

a.k.a. Fault Tolerance/Disaster Recovery. It's used to describe the resilience of cloud computing.

- The ability of a system to recover from failures and continue to function. This is done using two strategies:

	* Deploy resources in multiple locations
		- Global-scale computing
		- Protects against regional failure/disaster

	* No single point of failure
		- Resources in multiple locations
		- If one computer goes down, others pick up the load

**High scalability**

It's the process of adding moere resources on an as-needed basis, to automatically adjust resources to meet demand. We can:

*Scaling out*

It's adding more "mugs" to the pool of available "mugs" for our application.

*Scaling up*

It's making current resources bigger.

*Scaling down*

Horizontal scaling = Adding additional VMs/containers (scaling out)
Vertical scaling = Increasing power (e.g.: CPU/RAM) of existing VMs (scaling up)

The typical cloud model = Horizontal scaling

**Security**

- Full control of the security of our cloud environment. Patches, maintenance, network control, and more.

**Predictability**

* Predictable Performance and Costs
	- **Performance**
		* Consistent experience for customers regardless of traffic.
		* Autoscaling, load balancing, and high availability provide a consistent experience.

	- **Costs**
		* No unexpected surprises.
		* Track and forecast resource usage (costs) in real time.
		* Analytics provide patterns/trends to optimize usage.

**Governance**

- Standarized environments.
- Regulatory requirements.
- Audit for compilance.

**Manageability**

**Management of the cloud** (how we manage our different cloud resources):
	- Autoscaling
	- Monitoring
	- Template-based deployments

**Management in the cloud** (how we're able to manage and interact with our different cloud resources):
	- Portal
	- CLI
	- APIs

* **Security**
	- Full control of the security of our cloud environment. Patches, maintenance, network control, and more.

* **Governance**
	- Standarized environments.
	- Regulatory requirements.
	- Audit for compilance.

Resuming:

* High availability means systems are always available - even automatically!
* Reliability describes how Azure can tolerate failures or even disasters.
* Scalability refers to scaling out or scaling up while automatically provinding resources as needed.
* Predictability  is knowing our application will always perform as expected and knowing what it will cost.
* Security is having full control of our cloud security posture.
* Governance is standarizing cloud deployments to meet requirements/company standards.
* Manageability is management of cloud resources and how we interact with them.

## The economy of cloud computing

**Capital expenditure** (CapEx) => Large upfront investments

It's the money spent by a business or organization on acquiring or maintaining fixed assets, such as land, buildings, and equipment. In our scenario, taht could be buying more servers.

**Operational expenditure** (OpEx) => Pay-as-you-go

It's an ongoing cost for running a product, business, or system on a day-to-day basis, including annual costs.

We pay:
- Per execution
- Per second
- Combination of both above

Low usage = Low cost
* No lock-in fees. Exposure to Azure = Win Win

**Using the right budget in a compnay can enable huge change**:

- CapEx is buying HW outright, paid upfront as a one time purchase.
- OpEx is ongoing costs needed to run our business.
- Consumption-based pricing let's you pay only for what you use.


## Cloud service models

There are three types of cloud service model in the Azure context:

1) **Infrastructure-as-a-Service** (IaaS)
	- Infrastructure = actual servers (we don't have to go out and buy physical servers).
	- Scaling is fast
	- No ownership of hardawre
	- The IaaS offering includes VMs & servers, networking components, firewall and the physical HW runs on.

2) **Platform-as-a-Service** (PaaS)
	- It's a super set of IaaS.
	- It includes the same as IaaS, but also middleware, development tools, business intelligenc (BI), services, database management systems, and more.
	- It's designed to support the complete web application lifecycle: building, testing, deploying, managing and updating.
	- It avoids the expense and complexity of SW license hell

3) **Software-as-a-Service** (SaaS)
	- It includes boht IaaS and PaaS, and it's build on top of those.
	- It has to do with providing a service via a managed rented software service, such as Stripe for credit card payments, Gmail for emails, or QuickBooks for accounting.
	- Pay an access fee to use or might even be free.
	- No maintenance and latest features.

From Microsoft, in general, their most common SaaS offering is Office 365. From Azure, the app services Azure SQL, and Azure Active Directory are all examples of SaaS offering.

3) **Serverless** (extreme PaaS)
	- We're effectively using someone else's servers to run on.
	- Azure Functions is the best know serverless service.

This architecture takes PaaS to the most extreme by fully abstracting away the server, in such a way that a single function of code can be hosted, deployed, run, and
managed without even having to maintain a full application.

**Model**		**Characteristics**												**Examples**
--------------------------------------------------------------------------------------------------
IaaS			* Organization has complete control of the infrastructure.		VM, VNet, Storage
				* Dynamic and flexible. You can do almost everything.
				* Cost varies depending on consumption.
				* Services are highly scalable.
				* Multiple users share a single piece of HW.

PaaS			* Resources are virtualized and can easily be scaled up or		App Services, Azure
                  down as needed.												CDN, Cosmos DB
				* Services often assist with the development, testing and
				  deployment of apps.
				* Multi-users access via the same development application.
				* Integrates web services and databases.

SaaS			* Managed from a central location.								Microsoft Office 365
				* Hosted on a remote server.
				* Accessible over the Internet.
				* Users not responsible for HW or SW updates.
				* Rate limiting/QoS.



Normally, the people build their own SaaS products using Azure services.


**Shared Responsabilty Model**

			Physical 			Operating	Network		Identity and	Application		Information		Devices
			Infrastructure		System		Controls	Directory		Management		and Data		and Accounts


SaaS		MA					MA			MA			MA/You			MA				You				You
--------------------------------------------------------------------------------------------------------------------
PaaS		MA					MA			MA/You		MA/You			You				You				You
--------------------------------------------------------------------------------------------------------------------
IaaS		MA					You			You			You				You				You				You
--------------------------------------------------------------------------------------------------------------------
On-
Premises	You					You			You			You				You				You				You


**Service is the core of Azure, and there are three main ways to go about it**.

* IaaS provides servers, storage and networking as a service.
* PaaS is a superset of IaaS and also includes middleware, such as database management tools. It's here where a lot of the Azure benefits come into
  play for business.
* SaaS is when a service is built on top of PaaS, like Office 365.
* Serverless means that we don't have any servers. Let's a single function be hosted, deployed, run and managed on its own.


## Azure marketplace

**Benefits**

* Certified and less maintenance
Less maintenance than creating your own service or application from scratch. All marketplace offering are certified by Microsoft.

**Efficient**
It's much faster to build a project prototype by using ready-to-go services on the Marketplace.

**New markets**
You can venture into new markets by getting the full exposure of the Marketplace.

**Support**
There's both technical, design and architectural design support available when you list a service on the Marketplace.

## Cloud architect models

There are three general models which are considered:

**Private**
These services within the cloud are offered to selected users only, instead of the public.

*Pros*
- Complete controls of infrastructure.
- Benefits of public cloud.
- Better security and privacy, through both company firewalls and internal hosting.

*Cons*
- It's the organization IT department responsible for the cloud.
- Stafing

**Public**
It's Microsoft Azure, AWS, Google Cloud Platform, etc.

*Pros*
- No purchase of HW.
- Low monthly fees.

*Cons*
- No control over features and versions.
- No physical access.

**Hybrid**
It's a mix of private and public cloud.

*Pros*
- Avoid disruptions and outages.
- Adhere to regulation, governance, etc.
- Span both public and private cloud.
- Alleviate CapEx investments.

*Cons*
- Complex infrastructure.

# CHAPTER 03 - Azure Architecture

## Regions

"A region is a set of datacenters deployed within a latency-defined perimeter and connected through a dedicated
regional low-latency network".

**A set of datacenters** means that each region has more than one datacenter, which is a physical location. For
example:
East US has an official location of Virginia, but thre will be more than one datacenter there.

**Latency-defined paramter** is a techie way of saying not too far from each other. It's the time it takes data
to travel.

**Regional low-latency network** again means not too far. In today's money means a fiber connection between datacenters in the region.

Resuming:

REGION DEFINITION = Two or more datacenters + not too far from each other + connected with the fiber connection.

### How to choose a region

There are three main criterias to be aware of:

**Locations**
Choose a region closest to your users to minimize latency.

**Features**
Some features aren't in all regions. If you need a specific feature, some regions might be unavailable.

**Price**
Pricing is different from region to region.

**You will often have to choose wich is the most important: location, feature or price**.

## Paired region

1) **Each region is paired**
	- Within the same geographic area except Brazil South.
2) **Outage failover**
	- If the primary region has an outage you can failover to the secondary region.
3) **Planned updates**
	- Only one region in a pair is updated at any one time.
4) **Replication**
	- Some services used paired regions for replication.

###  Availability zones

- They are unique physical locations within an Azure region.
- Each zone is made up of one or more datacenters equipped with independent power cooling and networking.
- Each region that support Availabilty Zones, has a minumum of 3 separate zones.

Resuming:

* An Azure region is a set of datacenters that are close enough to each other that it doesn't matter which
  datacenter your data is in. You still get the same latency to your users.
  Latency is the time it takes data to travel.

* An Availability Zone is within a region, and each zone has its own separate power, colling and networking.
  You use Availabilty Zones to protect your data and applications from failures by replicating them between
  Availabilty Zones.

## Resource groups and Azure Resource Manager

## Demo: Creating Azure Resources