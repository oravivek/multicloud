# Create Oracle Database on Exadata Database Service@AWS

## Introduction

This lab walks you through the steps to provision an Oracle Database from OCI console.

Estimated Time:  30 Minutes

### Objectives

In this lab, you will learn to :

* Create Oracle Database on Exadata Database Service@AWS

### Prerequisites  

This lab assumes you have:

* Created Oracle Exadata Cloud Infrastructure
* Created Oracle Exadata VM Cluster

## Task 1: Provision Oracle Database

1. Launch the [Oracle Database@AWS](https://console.aws.amazon.com/odb/).

2. From the left pane, choose **Exadata VM clusters**.

3. Select the VM cluster that was created in previous lab - **my-vm-cluster**.

4. Click **Manage in OCI** to be redirected to the Oracle Cloud Infrastructure console.

5. On OCI cloud console, scroll down to **Databases** tab and click on **Create database** button.
    It will open a window to create a new database deploymnet - CDB and PDB.

    ![Create database](./images/create-database-od-aws.png)

6. Provide name for the container database(CDB) and unique name, which is optional.

    We have a choice to select latest version of databases i.e. 19c and 23ai.

    ![DB version details](./images/create-database-db-name.png "DB version details")

7. Specify database home, either a new database home or existing one.

    ![DB home details](./images/create-database-db-home.png "DB home details")
  
8. For database deployment, there are two options for database software image.

    * **Oracle Database Software Images** and
    * **Custom Database Software Images**

    ![Software image](./images/create-database-db-home-image.png "Software image")

  You can select database version from the available database versions.

    ![DB versions](./images/create-database-db-home-version.png "DB versions")

6. Provide administrator password for the database.

    You can use same password for the TDE wallet.
    
    ![Admin credentials](./images/create-database-admin-cred.png "TDE password ")

7. While provisioining database, you have an option to enable automatic backups on the database.  

    You can either **Amazon S3**, **Autonomous Recovery Service** or **Object Storage** for the database backups.

    ![Backups](./images/create-database-db-backups.png " Backups")

    * Provide inputs for the database backup retention window. 
    
    * You can specify deletion option for backups as well after the database is terminated. 

    * Select schedule for full backup and incremental backup as per requirements. 

    * You can also specify to initiate an immediate backup after database is provisioned. 

    ![Backup options](./images/create-database-backup-retention.png "Backup options")

8. In **Advanced-options** you can select, **Character set** and **National character set** if required.

    ![Advanced options](./images/create-database-advanced-options.png "DB Character SET ")

    In **Encryption** tab, please select an option for **Oracle-manged** or **Customer-managed keys**.

    Data will be encrypted with the key selected in this option. You can select customer-managed keys option , if you wan't to use your own keys for data encryption.

    ![Encryption key](./images/create-database-encryption.png "Encryption key")

9. Click **Create** after providing all inputs to deploy CDB and PDB.

10. After provisioning is complete, you can see the status of CDB and PDB as available.

    ![Provisioing completed](./images/create-database-db-details.png "Provisioing completed")

11. Go to **Pluggable Database** tab to view the Pluggable database.

    ![PDB Details](./images/create-database-pdb-details.png "PDB Details")

## Learn More

* Official documentation on [Oracle Exadata Database@AWS](https://docs.oracle.com/en-us/iaas/Content/database-at-aws/oaaws.htm)

## Acknowledgements

* **Author** - Vivek Verma, Master Principal Cloud Architect, North America Cloud Engineering
* **Last Updated By/Date** - Vivek Verma, July 2025
