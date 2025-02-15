<table class="tbl-heading"><tr><td class="td-logo">![](images/obe_tag.png)

June 13, 2019
</td>
<td class="td-banner">
# Lab 11: Accessing SQL Developer Web and Performance hub consoles on your dedicated autonomous database instance
</td></tr><table>

To **log issues**, click [here](https://github.com/oracle/learning-library/issues/new) to go to the github oracle repository issue submission form.

## Introduction

Oracle SQL Developer Web provides an integrated development environment and a database administration interface for Oracle databases in OCI. A web interface for Oracle SQL Developer, SQL Developer Web provides a subset of the features available for the desktop product and is bundled with various database services available in Oracle Cloud, including the dedicated autonomous database.

On the Performance Hub page of the SQL Developer Web console, you can monitor the performance of your Autonomous Database entities and ensure that these entities perform optimally.

This page allows you to view all the performance data available for a specific time period. Once a time period is selected, the database performance is displayed.

## Objectives

As an developer or DBA,

- Access OCI autonomous database console and get URL for sql developer web cosole
- Create a VNC connection to developer client VM and access sqldevweb console
- Access performance hub for your autonomous database instance



## Required Artifacts
- An Oracle Cloud Infrastructure account with access to Autonomous Transaction Processing console
- A pre-provisioned autonomous database with admin access
- A pre-provisioned developer client machine with network access to database

## Steps

### STEP 1: Access OCI autonomous database console and get URL for sql developer web cosole

Login to your Oracle Cloud Infrastructure account and navigate to the console page of your dedicated autonomous database. 

![access_db_console](./images/1000/access_db_console.png)

Navigate to the database details page and click the 'DB Connection' button

![db_connection](./images/1000/db_connection.png)

On the 'Database Connection' details page, select the 'Application Connection' radio button and copy the Access URL for SQL Developer Web as shown below


![sqldevweb_url](./images/1000/sqldevweb_url.png)

Save the URL some place while you work on the next step to access your developer client machine over VNC



### STEP 2: Create a VNC connection to developer client VM and access sqldevweb console 


 Since your autonomous database in a private network, you cannot access it with the URL above unless you are on a machine that has a network path to your database subnet. 

Lets connect to the developer client machine you setup in [Lab 6](./ConfigureDevClient.md) using a secure ssh tunnel

Open an ssh tunnel from your local laptop to your developer client. For instructions, refer to [Lab 6](./ConfigureDevClient.md)

**Mac or Linux users** can open a terminal window and create an ssh tunnel using the following command,

    ```
    $ ssh -N -L 5901:127.0.0.1:5901 -i \<priv-key-file\> opc@\<publicIP-of-your-devClient\> &
    ```

### For Windows users

- You can connect to and manage linux host mahine using SSH client. Recent versions of Windows 10 provide OpenSSH client commands to create and manage SSH keys and make SSH connections from a command prompt.

- Other common Windows SSH clients you can install locally is PuTTY. Click [here](https://docs.microsoft.com/en-us/azure/virtual-machines/linux/ssh-from-windows) to follow the steps to connect to linux host machine from you windows using PuTTY.

Once you have an ssh tunnel open, you can now access your developer client machine using VNC Viewer or any other VNC Client

- Open Firefox browser for the Applications menu top left and paste the SQL Developer Web Access URL you saved in Step 1

Note: Mac users should user CRTL + V to paste into VNC and not Command + V

- Provide the 'admin' username and password you created at the time of provisioning your database

![sqldevweb_login](./images/1000/sqldevweb_login.png)

- Click Sign In and should should now be looking at your SQL Developer Web Console

- Explore the SQL Developer Web interface and refer to its documentation for usage details

**Alternatively, you may also access the SQLDevWeb console of your dedicated ATP instance from your local web browser If you are in the same OCI Network / VCN as your database. For detailed instruction on setting up a VPN connection into your private database cloud infrastructure, refer to [Lab 5](ConfigureVPN.md)**



### STEP 3: Access the Performance Hub through SQL Developer Web Console

The SQL Developer Web home page provides quick links on the right to some of its key features, including the Performance Hub. 

Click on the Performance Hub tile to navigate to it. 

![performance_hub](./images/1000/performance_hub.png)

The Performance Hub consists of three major sections:

Time Selector field and Time Slider:
The Time Selector field is displayed on the top-right corner and performance data for the time selected in this field is displayed on the Performance Hub. By default, Last 60 mins is selected in this field.

![performance_hub_slider](./images/1000/performance_hub_slider.png)

The Time Slider on the Performance Hub shows the Active Sessions chart for the time period selected in the Time Selector field. The Active Sessions chart displays the average number of active sessions broken down by Wait, User I/O, and CPU. You can use the block on the Time Slider to select a shorter period of time for which data is displayed on the Performance Hub, and this is a subset of the period of time selected in the Time Selector field.

ASH Analytics tab:
The ASH Analytics tab shows Active Session History (ASH) analytics charts to explore ASH data. It allows you to drill down into database performance across multiple dimensions such as Consumer Group, Wait Class, SQL ID, and User Name. On the ASH Analytics tab, you can perform tasks such as:

Selecting an Average Active Sessions dimension and viewing the top activity for that dimension for the selected time period. For information on ASH, see Active Session History (ASH) in Oracle Database Concepts.
Generating an Automatic Workload Repository (AWR) report. For information on AWR, see Automatic Workload Repository (AWR) in Oracle Database Concepts.
SQL Monitoring tab:
The SQL Monitoring tab is not displayed by default and to view it, click SQL Monitoring on the Performance Hub.

![ash_analytics](./images/1000/ash_analytics.png)


The SQL Monitoring tab enables real-time SQL monitoring and allows you to view long running SQL statements in your Autonomous Database. On this tab, you can drill down into individual SQL statements, view the execution plan and the amount of database time being used by each SQL execution plan line, and identify and analyze resource intensive SQL statements. Note that SQL statements are only monitored if they've been running for at least five seconds or if they're run in parallel.

![sql_monitoring](./images/1000/sql_monitoring.png)

<table>
<tr><td class="td-logo">![create_exaSubnet](./images/obe_tag.png)</td>
<td class="td-banner">
### Fantastic ! You successfully learned to use the SQL Developer Web Console and Performance hub on your autonomous database instance.
</td>
</tr>


<table>