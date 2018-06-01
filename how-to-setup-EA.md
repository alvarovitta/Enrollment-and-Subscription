---
title: "How to set up and configure your organization's Enterprise Agreement"
description: Guidance for setting up and configuring an Azure Enterprise Agreement
author: petertay
---

# How to set up and configure your organization's Enterprise Agreement

Any Microsoft customer with a Microsoft Enterprise Agreement can add Azure to their Microsoft Enterprise Agreement (EA) by making an upfront monetary commitment to Azure. Funds deposited on account are used over the course of the year as Azure services are consumed.

## Defining the Enterprise Agreement

A Microsoft Enterprise Agreement is the foundation upon which to build your organization's Azure administration and governance policies.   
 
The Azure EA is organized by: 
 
* Departments 
* Accounts 
* Subscriptions 
 
The hierarchy design is an important consideration in billing reporting (see operations section).  While the hierarchy structure is not fixed, it can become challenging to change as workloads are expand and deployed. Engage the appropriate stakeholders during the design process and run through different usage scenarios. 
 
The figure below shows a sample hierarchy and structure of an Azure EA.  Each level of activity represented by the hierarchy is managed by an administrative role. 
 
![](../_images/how-to-setup-ea-1.png)

### Administrative roles

Use the four administrative roles listed below to manage the Microsoft Azure services under your enrollment. Use the corresponding Azure portal to administer the role: 

|Administrative Role|Role Description| Azure Portal|
|----------|----------|----------|
|Enterprise Administrator (EA)|The Azure EA policies are defined and managed by the Enterprise Administrator. There is no limit to the number of Enterprise Administrators.|[Enterprise Portal](https://ea.azure.com/)|
|Department Administrator (DA) |The DA can edit their assigned department details such as name and cost center. The DA also has the authority to manage and create accounts under the department within the enrollment. |[Enterprise Portal](https://ea.azure.com/)|
|Account Owner (AO) | The AO is the user who signed-up for the Azure subscription. Conceptually, the Account Administrator is the billing owner of the subscription. In RBAC, the Account Administrator isn't assigned a role. The AO is authorized to access the Account Center and perform management tasks which include: create new subscriptions,  cancel subscriptions, change the billing for a subscription, and change the Service Administrator|[Account Portal](https://azure.microsoft.com/en-us/)|
|Service Administrator (SA)|The SA is authorized to managed services in the Azure portal. By default, for a new subscription, the Account Administrator is also the Service Administrator. In RBAC, the Owner role is given to the Service Administrator at the subscription scope. |[Management Portal](http://portal.azure.com)|

### Additional information 
Use the following supplemental information as required: 
 
For more information on on-boarding and enrollment, see: Onboarding Guide to the Microsoft Azure Enterprise Portal (Direct Enrollment). 
 
For more information on Azure management concepts and to deploy, monitor, and manage solution resources as a group, see:  Azure Resource Manager Documentation. 
 

## Assigning the Enterprise Administrator Role 

Use the procedure described in this section to assign Enterprise Administrator roles. The information in this section is intended for: Licensing Administrator, Project lead, Technical Architect and Operations. The Enterprise Administrator (EA) is a key management role. The EA has full access privileges and visibility into all activities and resources of a corporate enrollment. The EA account is created at on-boarding and ideally, two people are assigned to the EA role. 

### Preparation  

Perform the following activities before you begin the procedure tasks:  
 
1. Consult with the following stakeholders to define the Enterprise Administrator role:
  * Finance:
    * Owns the customer policies and procedures and licensing related to changes to the Enterprise Agreement.  
    * Owns the customer policies and procedures related to payment of invoices related to Azure services.  
   * IT Security and compliance:  Owns the customer policies and procedures related to Privileged Access Management and Identity and, Access Management policy application. This stakeholder is responsible for the creation and management of Azure administration credentials.
2. Select two people to assume the Enterprise Administrator role.  
3. Create valid Azure Active Directory accounts for each EA role. Associate the EA accounts with a monitored mailbox. Enrollment and account notifications are sent to the Azure Active Directory account mailbox. Collect the information as shown in the following table: 

|Field|Value|
|-----|-----|
|Azure Tenant Name|tenant.onmicrosoft.com|
|Azure Tenant Administrator|tenant.adminl@contoso.com|
|Enterprise Administrator(s) Name|Lastname, Firstname| 
|Azure Active Directory Tenant Credentials|___@tenant.onmicrosoft.com|
|Enterprise Administrator Email |enterprise.admin@contoso.com|

### Procedure:  How to assign the Enterprise Administrator role  

Use this procedure to order cloud services, obtain credentials and initial access and assign administrator roles.  
 
1. Schedule a concierge on-boarding call (If assistance is required)
  * Schedule a concierge on-boarding call to receive an overview of Enterprise Azure, answer questions and get started. Either the customer or the Microsoft Account Team can perform this step.
    * Access the customer URL:  [http://aka.ms/AzureEntSupport](  )
    * Choose the problem type:  Onboarding
    * Choose the category:  Schedule an Onboarding or Concierge Session
    * Provide the Enterprise customer name and enrollment number, date and time and, attendees emails  
2. Activate the service
  * During the Azure services procurement process, a monitored corporate email address (not a consumer email provider) is specified to receive the invitation to activate.  
  * Refer to page four in the [Onboarding Guide to the Microsoft Azure Enterprise Portal](https://eaportalonboardingvideos.blob.core.windows.net/onboardingvideos/AzureDirectEACustomerOnboardingGuide_En.pdf) for instructions on how to start the activation process.
  * **Note:** If a different email address is needed to activate the enrollment request a new identity be added by submitting a incident request here. 
3. Select the Work Account authentication method
 * On the Enterprise Administrator Portal (https://ea.azure.com) landing page:
   * select the "Work Account" Authentication Mode
   * click the Sign-in button. 
4. Sign-in or sign-up
  * Use one of the login processes described below:
    * Sign In: Customers with existing tenant, or Azure, O365, D365, or VSTS Online
      * Contact the Azure tenant Azure administrators to obtain the cloud-based Azure Active Directory credentials.
      * Login to an existing tenant using cloud-based Azure Active Directory account. 
    * Sign-up: Customers without existing Microsoft cloud tenant (Azure Active Directory) and no Azure, O365, D365, or VSTS Online. Login using the email address listed in the invitation email that was sent and create a password that adheres to organizational policy. **Note:** You are creating your first Active Directory tenant. If you have an existing tenant, select Sign-in as described in the section below. 
 5. Assign enterprise administrators
   * A tenant administrator or initial existing enterprise administrator can assign additional enterprise administrators. See page eight in the [Onboarding Guide to the Microsoft Azure Enterprise Portal](https://eaportalonboardingvideos.blob.core.windows.net/onboardingvideos/AzureDirectEACustomerOnboardingGuide_En.pdf); Adding/Editing Enterprise Admins and Notification Contacts. **Note:** contact your Microsoft representative or create an incident request here if a notification is received indicating "The account provided is not a valid user of the Microsoft Azure Enterprise Portal". 
 
## Assigning the Department Administrator Role

Use the procedure described in this section to define Department Administrator (DA) roles and account structures. Organizations may want to split administration and costs by business units or other logical divisions. Azure refers to these divisions as Departments. An Enterprise enrollment can have many departments. Each department is assigned two Department Administrators. 

### Preparation 
Perform the following activities before you begin the procedure tasks:  
  
1. Consult the following stakeholders to define the Department Administrator role:
  * Department owners:  Responsible and accountable for the consumption of Azure services and related expenses
  * Finance:
    * Owns the customer policies and procedures related to changes to the Enterprise Agreement
    * Owns the customer policies and procedures related to payment of invoices related to Azure services
  * IT Security and Compliance:  Owns the customer policies and procedures related to Privileged Access Management and Identity and, Access Management policy application. This stakeholder is responsible for the creation and management of Azure administration credentials
2. Collect the department details as outlined in the following table:

|Field|Value|
|-----|-----|
|Department Name|Department Name|
|Cost Center|Cost Center|
|Spending Quota|Spending Quota ($)|
|Spending Notifications|Spending Notifications (%)|
3. Select two people to assume the role of Department Administrators.
4. Create valid Azure Active Directory accounts for each EA account. Associate the EA accounts with a monitored mailbox and collect the details as outlined in the table below. Enrollment and account notifications are sent to the Azure Active 
Directory account mailbox (as specified in the Enterprise Portal).

### Procedure:  How to create the department administrator roles and account structures 
 
Use this procedure to create the department and account structures. 
 
1. Sign-in to the Enterprise Administrator portal
  * Sign-in to the Enterprise Administrator Portal [https://ea.azure.com](https://ea.azure.com) as an Enterprise Administrator.
2. Define the Department / Account Structure
  * Follow the "Department/Account Setup Methodology" instructions on page nine of the [Onboarding Guide to the Microsoft Azure Enterprise Portal](https://eaportalonboardingvideos.blob.core.windows.net/onboardingvideos/AzureDirectEACustomerOnboardingGuide_En.pdf).
3. Create the department
  * Follow the "Manage Departments Panel" instructions found on page ten and the "Manage Department Detail" found on page eleven of the [Onboarding Guide to the Microsoft Azure Enterprise Portal](https://eaportalonboardingvideos.blob.core.windows.net/onboardingvideos/AzureDirectEACustomerOnboardingGuide_En.pdf).
  
## Assigning the Account Owner Role

Use the procedure described in this section to assign Account Owner (AO) roles to each department. Account Owners administer department subscriptions.

### Preparation 

1. Consult the following stakeholders as part of the Account Owner definition:
  * Department owners:  Responsible and accountable for the consumption of Azure services and related expenses.
  * Workload service owners: Owns the business requirements and drivers consumption of the different cloud services.
  * IT Operations owners:  Owns the customer policies and procedures related to IT Service Management and continuity of operations.
  * IT Security and compliance:  Owns the customer policies and procedures related to Privileged Access Management and Identity and, Access Management policies applicable to the creation and management of Azure administration credentials.  
2. Collect the AO and department details as outlined in the following table:

|Field|Value|
|-----|-----|
|Account Owner Name|Account Name|
|Department|Parent Department|
|Cost Center|Cost Center|
|Account Owner Azure AD Credentials|account.admin@tenant.onmicrosoft.com|
|Account Owner Email|account.admin@tenant.onmicrosoft.com|
|Is this an existing Account Owner|Yes/No|

### Procedure: How to assign the Account Owner role  

Use this procedure to create and validate ownership of an Account Owner role.    
  
1. Sign into the Azure account portal
  * Sign-in to the Account Portal using the account specified by the Enterprise Administrator, see:  [https://account.windowsazure.com](https://account.windowsazure.com).  
2. Associate an Account Owner with an email address
  * Associate the account with an existing, valid Account Owner. Enter the email address associated with the account. Alternatively, associate a new Account Owner by entering a new, valid email address.  
3. Confirm account ownership
  * Confirm the account ownership was created. The owner of the email address provided in the previous step receives a notification that they have been invited to activate their account in the enrollment.
4. Activate account ownership
  * Activate the account ownership by signing in to the Enterprise Portal with the Account Owner email address provided. Receipt of email notification is not required for login. Valid Account Owners can log into the Azure Enterprise Administrator Portal: [https://ea.azure.com](https://ea.azure.com).

## Assigning the Service Administrator Role

Use the procedure described in this section to create a subscription and assign a Service Administrator (SA) role. Azure services are provisioned within subscriptions. Those services are managed within the context of the subscription by the service administrator. By default, the account owner is the service administrator on any new subscriptions.

### Preparation

1. Consult the following stakeholders as part of the Account Owner definition:
  * Department owners:  Responsible and accountable for the consumption of Azure services and related expenses.
  * Workload service owners: Owns the business requirements and drivers consumption of the different cloud services.
  * IT Operations owners:  Owns the customer policies and procedures related to IT Service Management and continuity of operations.
  * IT Security and compliance:  Owns the customer policies and procedures related to Privileged Access Management and Identity and, Access Management policies applicable to the creation and management of Azure administration credentials.  
2. Collect the AO and department details as outlined in the following table:

|Field|Value|
|-----|-----|
|Subscription Name|Subscription Name|
|Account|Parent Account|
|Department|Parent Department|
|Service Administrator AD Credentials|service.admin@tenant.onmicrosoft.com|
|Service Administrator Email|service.admin@tenant.onmicrosoft.com|Co-Service Administrator AD Credentials|coservice.admin@tenant.onmicrosoft.com|
|Co-Administrator Email|coservice.admin@tenant.onmicrosoft.com|
|Offer|Microsoft Azure Enterprise, Dev/Test|

### Procedure: How to assign the Service Administrator role  
  
Use this procedure to assign a Service Administrator (SA) to the enrollment.

1. Open the Account Portal
  * Sign-in to the Account Portal [https://account.azure.com](https://account.azure.com) as the Subscription Administrator.
2. Create a subscription
  * To create a subscription, use the "Adding a New Subscription" instructions shown on page 25,  [Onboarding Guide to the Microsoft Azure Enterprise Portal](https://eaportalonboardingvideos.blob.core.windows.net/onboardingvideos/AzureDirectEACustomerOnboardingGuide_En.pdf).
3. Assign a Service Administrator
  * To assign a Service Administrator, use the "Edit Subscription Detail" instructions shown on page 27,[Onboarding Guide to the Microsoft Azure Enterprise Portal](https://eaportalonboardingvideos.blob.core.windows.net/onboardingvideos/AzureDirectEACustomerOnboardingGuide_En.pdf). **Note:** designate separate individuals as Service Administrators of sandbox and production subscriptions.

## Defining Subscriptions and Patterns

A subscription is a logical limit of scale by which resources can be allocated. These limits include hard and soft caps of various resource types (for example, 10,000 compute cores per region per subscription in the Azure Resource Manager model). A subscription 
additionally forms a top-level billing unit.    

### Subscription and account management  
 
The figure below shows the hierarchy and management structure for each subscription. Subscriptions are managed as follows: 
 
* The Account Owner manages each account and associated subscription through the Account Portal. 
* An account can have one or more associated subscription.   
* Only the Account Owner has the ability to create subscriptions.   
* Creating different subscriptions and assigning a different Service Administrator and 
* Co-Administrators to each subscription provides controlled access to development projects and environments within the organization.  
  
### Subscription patterns  

A pattern is subscription design template that is based on the needs of the organization. This guide describes the following pattern 
scenarios:  
  
* Sandbox Pattern: Use when learning how to use Azure and build subscriptions.    
* Sandbox +  Production: Use to create a separate subscription to deploy production workloads.  
* Sandbox + Production + Purpose Built:  Use for organizations that require a separate, production-ready subscription for running workloads.  
* Continuous Development Lifecycle: Use to maintain isolated sandbox subscription and production workloads. 
 
### Additional information  
For information on subscription structure, see  Onboarding Guide to the Microsoft Azure Enterprise Portal. Refer to "Subscription Setup Methodology" on page 23.  

## Designing the subscription

Use the procedure in this section as the basis on which to design a subscription. For more information on design considerations and proven practices, see Additional information in this section. 
  
When designing the subscription model, consider that your organization's subscription enrollment is likely to expand and grow more 
complex over time. Your subscription enrollment strategy should be scalable and adaptive.   
  
### Preparation  

Perform the following activities before you begin the procedure tasks:  

  
1. Consult the following stakeholders as part of the subscription definition:  
  * Service Owners:  
  * IT Operations owners:  Owns the customer policies and procedures related to IT Service Management and continuity of operations  
  * Workload and Application owners: Owns the business requirements and driver of consumption of the different cloud services  
2. Collect the subscriber details as outlined in the following table:  

|Field|Value|
|-----|-----| 
|Subscription Name|<Subscription Name> |
|Pattern|Sandbox, Production, Purpose Built|
|Account|<Parent Accoun>|
|Department|<Parent Department>| 
|Service Administrator Azure AD Credentials|<service.admin@tenant.onmicrosoft.com>| 
|Service Administrator Email|<___@tenant.onmicrosoft.com>| 
|Subscription Type|Microsoft Azure Enterprise, Dev/Test*| 

*Enterprises can identify an account and a subscription to host DevTest Workloads at a discounted rate. 

### Procedure: How to design a subscription  
  
Use this procedure to design a subscription.  
  
1. Define the subscription structure  
  * Refer to the following subscription patterns:   
    * Using the Sandbox Pattern  
    * Using the Sandbox + Production Pattern   
    * Using the Sandbox + Production + Purpose Built Pattern  
    * Using the Continuous Development Lifecycle Pattern  
  * See Subscription Setup Methodology, page 23:   Onboarding Guide to the Microsoft Azure Enterprise Portal 
2. Leverage Dev/Test subscriptions  
  * Refer to:  Video: Enabling EA DevTest Subscriptions in the EA Portal  
3. Create the subscription and assign a Service Administrator 
  * Access the Account Portal and follow the steps described in: Assigning the Service Administrator Role. 
4. Designate an RBAC Owner  
  * Add an RBAC Owner administrator for a subscription in Azure portal, see:  Manage Administrator Roles - Add an RBAC Owner  
5. Add or change a Co-administrator  
  * Using the Azure portal, designate a co-administrator, see:  Manage Administrator Roles - Add or Change Co-Administrator  
6. Change the Service Administrator for an Azure subscription  
  * See:  Manage Administrator Roles - Change the Service Administrator  
7. Change the Account Administrator for an Azure subscription  
  * See:  Manage Administrator Roles - Change the Account Administrator  
  
### Additional information  
Use the following supplemental information as required:  
 
Review the following: Azure enterprise scaffold - prescriptive subscription governance   
 
Take subscription limits under consideration when planning for subscription designs. See subscription limits at: Azure subscription and service limits, quotas, and constraints  
 
Design considerations: 
When planning to have multiple Azure subscriptions, consider the complexity implications including:  
* Duplicate provisioning and management: IP Address space, network circuits, gateways, vNets, Subnets, NSGs, routing  
* More connectivity to manage   
* More security to manage  
* More identities to manage  
* Potentially more ExpressRoute (ER) circuits to buy  
 
Proven practices:  
* Plan for multiple subscriptions  
* Start with one subscription; try to minimize the number of subscriptions; add additional subscriptions based on requirements  
* Minimize the number of subscription owners  
* Refrain from assigning one account owner across multiple subscription types  
* Use Azure Active Directory for Azure Governance roles  
* Use Built-In Roles before Custom Roles  
* Create Custom RBAC Roles only if Built-in does not exist  
* Use groups to assign RBAC versus users  
* Take network requirements and Express Route boundaries into account

## Using the Sandbox Pattern 

Use the Sandbox Pattern when learning to use Azure.  
  
The Sandbox scenario is designed:   
* to provide an environment for learning and experimentation for non-production workloads   
* to provide an isolated network environment  
* to support easy build-up and tear-down of infrastructure resources as a single, trust-worthy Azure AD tenant for use with a single sandbox account owner assigned  
  
The following table provides a profile description for the personas who use this pattern:   
|IT Operations|Security/Compliance Officer|Finance/Business|Development Manager|
|-----|-----|-----|-----| 
|Need: a sandbox environment to easily and quickly provision resources for non-production workloads.|Need segregation of access controls from production workloads|Need: to leverage discounted subscription for sandbox environments|Need:  self-service environment to experiment with azure features/functionality that can be easily be setup and torn down| 
### Additional information  
Consider the following supplemental information for this pattern:  
  
Advantages:  
* vNet address spaces can be tailored per application without risk of network address space conflicts  
* Lower cost on Dev Test Subscriptions  
* Minimal risk of affecting production workloads  
  
Disadvantages:  
* Granulated Application RBAC model  
* Requires little to no capacity planning  
* No access to corporate services

## Using the Sandbox + Production Pattern 

Use the Sandbox + Production Pattern once you are ready to deploy production workloads in Azure. You can use this pattern where you will create a separate subscription when deploying production workloads. 
 
The Sandbox + Production Pattern has the following properties: 
* each environment contains different types of applications (sandbox/non-prod and production) 
* subscriptions are network isolated from one another 
* virtual networks will wrap the different applications for traffic separation 
* subscription have different pricing models 
* both subscriptions trust 1 single Azure AD tenant 
* each subscription contains a separate Azure AD account owner (see Service Administrators section) 

Stakeholders: 
* Service Owners  
* IT Operations Owners 
* Security/Compliance Officer 
* Workload & Application Owners 
* Finance 
 
The following table provides a profile description for the personas who use this pattern:   
|IT Operations|Security/Compliance Officer|Finance/Business|Development Manager|
|-----|-----|-----|-----|  
|Need: a production environment that is network isolated from sandbox environment to avoid administration mistakes from affecting production.|Need: a separate access control mechanisms to ensure staff with access to sandbox environment don’t also have access to production environment|Need: to leverage discounted subscription for sandbox environments|Need: isolated self-service environment to experiment with azure features/functionality that can be easily be setup and torn down  
  
### Additional information  
Consider the following supplemental information for this pattern:  
 
For more information on Azure limits, see: Azure subscription and service limits, quotas, and constraints 
 
Advantages:  
* vNet address spaces can be tailored per application without risk of network address space conflicts  
* Environment isolation  
* Lower cost on DevTest subscriptions  
  
Disadvantages:  
* Multiple environment to manage 
* Granulated Application RBAC model  
* Requires medium capacity planning

## Using the Sandbox + Production + Purpose Built Pattern 

Use the Sandbox + Production + Purpose Built Pattern for organizations that require a separate, production-ready subscription for running workloads.  
 
The defined governance and controls for standard sandbox and production workloads do not apply, for example: a research project that is managed by a separate entity, or for different regulation requirements, or where controls are applied differently. 
 
The Sandbox + Production + Purpose Built Pattern has the following properties: 
* a separate production environment (purpose-built) that is separate from the main production environment 
* each environment contains different types of applications (sandbox/non-prod, production, and purpose-built) 
* environments are isolated from each other 
* virtual networks will wrap the different applications for traffic separation 
* each subscription trusts a single Azure AD tenant 
* each subscription contains a separate Azure AD account owner (see Service Administrators section) 
 
The following table provides a profile description for the personas who use this pattern:   
|IT Operations|Security/Compliance Officer|Finance/Business|Research Scientist|
|-----|-----|-----|-----| 
|Need: a production-ready environment that leverages newest Azure Emerging functionality in regions not supported in my corporate environment."|Need: production environment with segregated access to abide by specific compliance regulations and to enforce more strict security controls than my regular corporate environment|Need: to fund and track budget allocation which differs from corporate environment|Collaborate with external organizations, leverage external data sources and networks, provision and run scientific workloads. |
 
### Additional information  
Consider the following supplemental information for this pattern:  
 
Advantages:  
* Vnet address spaces can be tailored per application 
* Environment Isolation  
* Lower cost on Dev Test Subscriptions 
 
Disadvantages: 
* Multiple environments to manage 
* Granulated Application RBAC model for Azure 
* Double Azure AD RBAC and Operations effort 
* Additional complexity with multiple AADs 
* Requires medium capacity planning 

## Using the Continuous Development Lifecycle Pattern 

Use the Continuous Development Lifecycle Pattern to maintain isolated sandbox subscription and production workloads. Subscriptions can be used for the purposes of code promotion approaches. 
 
The Continuous Development Lifecycle Pattern has the following properties: 
* Each environment contains the different types of applications.  
* Virtual Networks will wrap the different applications for traffic separation.  
* Subnets will be created within each environment to establish required security isolation zones among application tiers.  
* Each subscriptions trust 1 single Azure AD tenant. 
* Each subscription contains a separate Azure AD account owner (see Service Administrators section). 
* Dev subscription contains separate subnets and resource groups that isolate (Test, Dev and QA environments). 
 
 
The following table provides a profile description for the personas who use this pattern:   
|IT Operations|Security/Compliance Officer|Finance/Business|Development Manager|
|-----|-----|-----|-----|  
|Need: to connect DevOps environment to production to facilitate code promotion between environments, plus a sandbox environment that is network isolated from production environment to avoid administration mistakes from affecting production|Need: separate access control definitions to ensure staff with access to sandbox environment don’t also have access to production environment. Connections and network traffic between DEV and PROD subscriptions should be managed|Need: to leverage discounted subscription for sandbox and dev environments |Need: isolated self-service environment to experiment with azure features/functionality that can be easily be setup and torn down |
 
### Additional Information 
Consider the following supplemental information for this pattern:  
 
Advantages:  
* Streamlined Continuous code deployment 
 
Disadvantages: 
* Multiple environments to manage 
* Granulated Application RBAC model 
* Requires medium capacity planning 
* Complex Vnet addressing 
* Mistake in management could affect all environments

# Defining Resource Groups

A Resource Group is a logical container in which you can pool and categorize your resources. Resource groups are also used to manage access control. 
 
Resource Group examples:  
* Billing 
* Security 
* Web servers 
* Compute resources 
* Applications 
 
The following figure illustrates the association between the Subscription Administrator and subscription. 
 
## Additional information 
Consider the following supplemental information:  
 
Links: 
https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-group-overview#resource-groups 
https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-group-portal

## Designing a Resource Group

Use the procedure in this section to design a Resource Group. 
 
### Preparation 
Perform the following activities before you begin the procedure tasks:  
1. Consult the following stakeholders as part of the subscription definition: 
  * Workload service owners:  Owner of the business requirements and driver of consumption of the different cloud services. 
  * Fabric administrator:  [to be defined, replaced, or removed] 
  * IT Operations Owners:  Owner of the customer policies and procedures related to IT Service Management and continuity of operations. 
  * IT Security and Compliance:  Owner of the customer policies and procedures related to information classification and handling, security monitoring and controls, and security incident management.
2. Collect the subscriber details as outlined in the following table:  

|Field|Value|
|-----|-----| 
|Resource Group Name|< Resource Group Name>| 
|Location|<Azure Region>| 
|Subscription Name|<Parent Subscription Name>| 
|Contributor Permission|<___@tenant.onmicrosoft.com>| 
|Owner Permission|<___@tenant.onmicrosoft.com>| 
|Reader Permission|<___@tenant.onmicrosoft.com>| 
 
### Procedure:  How to create a Resource Group 
 
Use this procedure to create a resource group. The Service Administrator uses the Azure Portal or ARM 
templates. 
 
1. Define the Resource Group model 
  * For recommended patterns, refer to:  
    * Using the Agile IT Workloads Pattern 
    * Using the Traditional IT Workloads Pattern 
    * Using the Access Management Grouping Pattern 
2. Access the Azure portal 
  * Create and Manage Resource Groups, see: Manage Azure resources through portal. 
3. Create an Azure resource group 
  * Refer to: Azure Resource groups using PowerShell  
  * Use the command: New-AzureRmResourceGroup commandlet 
4. Create an Azure Accelerator resource group with tags 
  * GitHub:  AzureAccel/Scripts/ResourceGroupCreation.ps1  
 
### Additional information 
Consider the following supplemental information:  
 
For information on service limitations, see:  Azure subscription and service limits, quotas, and constraints. 
 
Design considerations: 
* All the resources in your group should share the same lifecycle. You can deploy, update, and delete them together. If one resource, such as a database server, needs to exist on a different deployment cycle it should be in another resource group. 
* Resources must belong to a single resource group. 
* A resource group can contain resources that reside in different regions. 
* A resource group is tied to a subscription. A resource group cannot span subscriptions. Once you assign a resource to a resource group, you can move it out, but it can't span multiple subscriptions. 
* A resource can interact with resources in other resource groups. Interaction is common when the two resources are related but do not share the same lifecycle (for example, web apps connecting to a database). 
* A resource group can be used to scope access control for administrative activities. You can apply RBAC permissions at the subscription level or at the resource group level. Anything assigned at the subscription level will be inherited at the resource group level. 

Proven practices: 
* The resource group design should follow Agile IT workload designs which include:  Web tier, application tier, data tier, management tier. 
* Assign permissions at the resource group level as opposed to assigning them at the subscription level. 
* Use tagging within your resource groups to ensure categorization of resources for billing and security purposes. 
* Use a cohesive and consistent naming standard of your security groups across your subscriptions. 
* When creating resource groups, ensure that specific tiers (web, app, data, management) of the workload are assigned to the same region.

## Using the Agile IT Workloads Pattern

Use the procedure in this section to create a resource group design pattern that matches the lifecycle of your Agile IT workload layers. The resource groups reflect the layers of deployment in the workload (web, app, data, management tiers).   
 
If an application is composed of a set of web servers, app servers and, database servers you can identify the corresponding resource groups needed for that application as: web, app, and database resource groups. 
 
### Preparation  
No preparations required.  
 
### Procedure: How to create an Agile IT workloads pattern  
  
Use this procedure to design an Agile IT workloads pattern.  
 
1. Define the Resource Group model 
Review the guidance and patterns provided in this section. 
 
2. Create and Manage Resource Groups 
Refer to:  Manage Azure resources through portal. 
3. Create Azure Resource Group using 
  * Use the: New-AzureRmResourceGroup commandlet. See:  Azure Resource groups using PowerShell 
  * Example: Create two resource groups across two different regions in same subscription 
  * PS> Select-AzureRmSubscription -Subscription $ProductionSubscription New-AzureRmResourceGroup -Name $WebTier -Location CanadaEast New-AzureRmResourceGroup -Name $DatabaseTier -Location CanadaCentral 
 
### Additional Information 
Consider the following supplemental information for this pattern:  
 
Advantages: 
* IT workload components are grouped base on the function they provide to that workload 

Disadvantages: 
* Additional management overhead in having to administer several: 
* Network security groups (NSGs) 
* RBAC 
* Resource policies 

## Using the Traditional IT Workloads Pattern 

Use this pattern to group Traditional IT workloads by the items within the same lifecycle, such as an application. Grouping by application allows for individual application management. 

### Preparation  
No preparations required.  

### Procedure: How to create a Traditional IT workloads pattern  
  
Use this procedure to design a traditional IT workloads pattern.  
Link to < how to create> 
Link to <Sample Scripts> 
 
### Additional information 
Consider the following supplemental information for this pattern:  
 
Advantages: 
* All resources that support an application are contained within the same resource group. 
 
Disadvantages: 
* An error in administration could affect all application resources within a resource group 
* No ability to segregate network traffic between application components 
* Access granted at the resource group level provides access to all resources within an application 

## Using the Access Management Grouping Pattern

Use this scenario when there is a need to create resource groups that is based on access management needs. You can grant access at resource groups when appropriate. 
 
### Preparation  
No preparations required.  

### Procedure: How to create an access management grouping pattern  
  
Use this procedure to design an access management grouping pattern.  
Link to < how to create> 
Link to <Sample Scripts> 

### Additional information 
Consider the following supplemental information for this pattern:  
 
Advantages: 
* More granularity 
* Aligns with resource-specific roles 
* Ongoing manageability 
 
Disadvantages: 
* Difficult to understand dependencies between resources and the workloads they support. 