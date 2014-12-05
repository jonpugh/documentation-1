---
title: Restoring an Environment from a Backup
filename: source/_common-tasks/restoring-an-environment-from-a-backup.md
---

Each site environment's backups can be found on the Backups subtab for the environment in the Pantheon Dashboard.  


 ![Backup Subtab](https://pantheon-systems.desk.com/customer/portal/attachments/169631)

## Restoring an environment from its own backup

Each manual and automatic backup can be directly restored to that environment from the Pantheon Dashboard by clicking the **Restore** button to the right of a backup. ![Backups and Restore Button](https://pantheon-systems.desk.com/customer/portal/attachments/169624)

This is a  **destructive ** process; this will  **wipe** your database and files, and restore them from the backup.

When a restore starts, the operation is placed in a machine queue and executed. Depending on the size of the site, this operation may take some time; be patient and do not attempt to restart the restore unless you are confident that it completed. When in doubt, submit a support ticket and ask.

Pantheon does not recommend directly restoring a live environment from a backup; instead, restore to dev or test, then pull the code change and clone the content to live. This will minimize user-facing downtime.

## Restoring an environment from another environment's backup

If you want to restore a different environment than the source, you have two options.

1. Download all three backup parts (Code, Database and Files) from the source environment, upload the Database and Files to the target environment, then update code.
2. Download the Code backup and use temporary links for the Database and Files to import Database and Files to the target environment, then update code.

Regardless of the option you choose, restoring is basically the same process.

In the source environment, find the backup that you wish to retrieve, then for each of the three backup parts  (Code, Database and Files), click the download link:

![Temporary backup link](https://pantheon-systems.desk.com/customer/portal/attachments/169628)  







    wget "https://pantheon-backups.s3.amazonaws.com..."

## Importing existing content

Once you have the downloaded parts and/or links, navigate to the target environment and click on the Workflow subtab.  




![Workflow Tab](https://pantheon-systems.desk.com/customer/portal/attachments/169632)  











