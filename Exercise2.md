# Getting started with Hyperscale (Citus) extension for PostgreSQL

## **Lab 1: Getting started with Hyperscale (Citus)**

For a successful connection into Hyperscale (Citus) on Azure Database for PostgreSQL, we will be adding firewall rules to allow access to our Hyperscale (Citus) database.

### Task 1: Configure server-level firewall service

Follow the instructions given below to allow yourself access to the Hyperscale (Citus) server group.
 
1.In the **Azure Portal** go to **Home**, then locate **Azure services** and select **Azure Database for PostgreSQL servers** on homepage.

![](images/azpostgresql.png)


2.Click on your PostgreSQL Database **postgreXXXXX**.

![](images/azpostgresql1.png)

3.We pre-provisioned a basic production grade Hyperscale (Citus) cluster with 1 coordinator with 4 vCores and 16GB RAM and 2 workers with each 2 vCores and 16GB RAM for this lab. You can review the cluster details in Azure Portal. 

![](images/azpostgresqlclusterinfo.png)


4.On the overview blade under **Security** click **Networking** and put **Allow Azure Service** to **YES**.

![](images/2postgresqlfw.png)

5.Now add **Firewall Rule**. Select **Add current client IP address**, this will add the client IP by creating a new rule. Then **save** the changes.

![](images/firewallip1.png)

6.Click **Next** on the bottom right of this page.
