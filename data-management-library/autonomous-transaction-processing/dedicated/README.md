<table class="tbl-heading"><tr><td class="td-logo">[![](images/obe_tag.png)](README.md)

Last Updated:<br>August 4, 2019
</td>
<td class="td-banner">
# Working with Autonomous Transaction Processing - Dedicated
</td></tr><table>

Oracle's Dedicated Autonomous Transaction Processing service allows an organization to Rethink Database IT, enabling a customizable private database cloud in the public cloud. The dedicated choice makes it possible to deliver a self-service database capability that aligns with organizational structure. Different lines of business or project teams can have complete autonomy in their individual execution while the company itself gets a fleet wide simplified aggregation of overall health, availability and cost management. This separation of Fleet vs Database administration allows simple budgeting controls and resource isolation without getting in the way of the line of business execution. And a dedicated database deployment will support the entire spectrum of needs from simple apps to apps that require the highest governance, consistent performance and operational controls.


These hands-on lab guides provide step-by-step directions to setting up and using your dedicated Autonomous database platform in the Oracle Cloud Infrastructure. 

Lab 1 deals with setting up the network, users and groups and requires administrator privileges on your OCI account.

Labs 2 & 3 are geared towards the fleet administrator role responsible for deploying the autonomous exadata infrastructure and container databases.

Labs 4 onwards are intended for a regular database user, DBA or developer who simply want to spin up an autonomous database in one of the pre-provisioned containers and start building applications.

## Goals for this workshop
- Prepare your private network in the Oracle Cloud Infrastructure
- Provision Exadata Infrastructure in a private OCI network
- Provision an Autonomous Container Database
- Provision databases on your dedicated Autonomous Infrastructure
- Setup VPN Connectivity to your Autonomous Exadata Infrastructure
- Configure a development system for use with your dedicated autonomous database
- Build and deploy Python application stacks on dedicated autonomous infrastructure
- Build and deploy node.js application stacks on dedicated autonomous infrastructure
- Build and deploy Java application stacks on dedicated autonomous infrastructure
- Use OCI CLI commands to work with your Autonomous databases
- Invoke and use the sqldevweb console
- Build apex applications on dedicated autonomous database
- Manage database & performance using SQL Developer Web and Performance Hub
- Migrate an on-prem application schema using Data Pump
- Setup live migration of business critical databases using Oracle Goldengate replication

<!-- # How to Get Your Free Cloud Trial Account
Please click on the following link to create your <a class=“trial-link” href="https://myservices.us.oraclecloud.com/mycloud/signup?language=en&sourceType=:ex:tb:::RC_NAMK181011P00041:ATPHOL&SC=:ex:tb:::RC_NAMK181011P00041:ATPHOL&pcode=NAMK181011P00041" target="_trial">Free Account</a>, and complete all the required steps to get your free Oracle Cloud Trial Account. When you complete the registration process you'll receive a $300 credit that will enable you to complete the lab for free.  Additionally, you'll have 1000s of hours left over to continue to explore the Oracle Cloud.

  - Soon after requesting your trial you will receive the following email. You may begin working on Lab 100. -->

  <!-- ![](images/readme/code_9.png) -->



# Workshop Overview

## Before You Begin
**What is an Autonomous Transaction Processing Dedicated?**

The dedicated infrastructure feature of Oracle Autonomous Transaction Processing enables you to create an Oracle Autonomous Database platform that is private and isolated to your use all the way down to the Oracle Exadata hardware running your database instances and storing your database data.

You define and use Oracle Cloud Infrastructure Networking and IAM (Identity and Access Management) resources to ensure secure and authorized use of your dedicated Autonomous Transaction Processing databases and the database resources that underlie them.
<!-- Oracle Autonomous Transaction Processing Dedicated ...  

Read on to begin your Getting Started journey with Oracle Autonomous Transaction Processing Dedicated. -->

**You are all set, let's begin!**


## Lab 1: Preparing your private network in the Oracle Cloud Infrastructure

**Key Objectives**:
- Create compartments and user groups with the right set of access policies for separation of duties
- Create fleet admin and database user accounts
- Layout a secure network for the database and application infrastructure

**[Click here to run Lab 1](ATPD-Networking.md)**


## Lab 2: Provisioning Exadata Infrastructure for Autonomous DB in OCI

**Key Objectives**:

As a fleet administrator, 
- deploy an Autonomous Exadata Infrastructure in a pre-provisioned private network in your OCI account
- Understand AEI maintenance scheduling
- Understand database licensing options

**[Click here to run Lab 2](ProvisionAEI.md)**


## Lab 3: Provisioning an Autonomous Container Database

**Key Objectives**:

As a fleet administrator,
- Deploy an Autonomous Container Database (ACD) onto an Autonomous Exadata Infrastructure (AEI)

**[Click here to run Lab 3](ProvisionACD.md)**


## Lab 4: Provisioning databases on your dedicated Autonomous Infrastructure

**Key Objectives**:

As a database user, DBA or application developer,

- Rapidly deploy autonomous transaction processing databases
- Manage your database backups

**[Click here to run Lab 4](ProvisionADB.md)**

## Lab 5: Configuring VPN connectivity into your private ATP network

**Key Objectives**:

As a fleet / network admin,

- Configure a VPN server in OCI based on OpenVPN software
- Configure your VPN client and connect to VPN Server

As a database admin / user,
- Configure your VPN client and connect to VPN Server
- Launch SQL Developer on client and connect to a dedicated ATP instance

**[Click here to run Lab 5](ConfigureVPN.md)**


## Lab 6: Configuring a development system for use with your dedicated autonomous database

**Key Objectives**:
As a database user, DBA or application developer,
- Configure a secure connection from your application instance to your dedicated autonomous database using Oracle SQL Developer, SQLCL and SQL*Plus.

**[Click here to run Lab 6](ConfigureDevClient.md)**

## Lab 7: Building and deploying node.js application stacks on dedicated autonomous infrastructure

**Key Objectives**:

As an application developer,
- Learn how to deploy a node.js application and connect it to your dedicated autonomous database instance

**[Click here to run Lab 7](BuildNodeApps.md)**

## Lab 8: Building and deploying Python application stacks on dedicated autonomous infrastructure

**Key Objectives**:

As an application developer,
- Learn how to deploy a python application and connect it to your dedicated autonomous database instance

**[Click here to run Lab 8](BuildPythonApps.md)**

## Lab 9: Building and deploying Java application stacks on dedicated autonomous infrastructure

**Key Objectives**:

As an application developer,
- Learn how to deploy a java application and connect it to your dedicated autonomous database instance


**[Click here to run Lab 9](BuildJavaApps.md)**

## Lab 10: Using CLI commands to work with your Autonomous databases

**Key Objectives**:

As an application developer, DBA or DevOps user,

- Create/Destroy your autonomous database instances using a command line interface
- Interact with Oracle Cloud Infrastructure resource using a CLI instead of a web console


**[Click here to run Lab 10](OCI-CLI.md)**

## Lab 11: Using sql*developer web console

**Key Objectives**:

As an application developer, DBA or DevOps user,

- Access OCI autonomous database console and get URL for sql developer web cosole
- Create a VNC connection to developer client VM and access sqldevweb console
- Understand features of sqldevweb

**[Click here to run Lab 11](SQLDevWeb.md)**

## Lab 12: Building Apex application on dedicated autonomous database

**Key Objectives**:

As an application developer, DBA or DevOps user,

- Access OCI autonomous database console and get URL for apex web cosole
- Create a VNC connection to developer client VM and access apex on your database as admin user
- Setup additional apex developer users 

**[Click here to run Lab 12](Apex.md)**

## Lab 13: Migrating to Dedicated ATP using Data Pump

**Key Objectives**:

As a database admin or user,

1. Download a sample datapump export dump file from Oracle Learning Library github reposiory.
2. Upload .dmp file to OCI Object storage bucket.
3. Setup cloud credentials and use data pump import to move data to your ATP database.

**[Click here to run Lab 13](DataPump.md)**

## Lab 14: Live migration to ATP-Dedicated using Oracle Goldengate replication


**Key Objectives**:

As a database admin,

- Install Golden Gate on both source and target database
- Configure extract,pump and replicat processes on source and target golden gate instances respectively
- Replicate real time data from a simulated on-premise database to ATP-Dedicated

**[Click here to run Lab 14](Goldengate.md)**