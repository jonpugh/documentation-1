---
title: Cloning an Existing Site from a Dashboard Backup
description: Detailed information on how to make a copy of your existing Drupal or WordPress site code, files, and database.
category:
  - developing
keywords: clone, restore backup, clone existing pantheon site, clone from pantheon backup, clone pantheon site, copy pantheon site
---
All Pantheon sites consist of three parts:

* **Code**: The code that makes up your site and contained within your Pantheon Git repository.
* **Files**: Images, user uploads, and other files that are not stored in version control, located in /sites/default/files (Drupal) or /wherever/wp-uploads/go (WordPress).
* **Database**: The MySQL database utilized by your code to store content, settings, etc.

## Copy Your Code/Files/Database

1. From your Site Dashboard, go to the Live environment and click **Backups**.
2. Select the backup you want to clone from, and download each of the backup files (code, database, files) by clicking the **download** icon.

Code archives contain the full remote Git repository and reflect the state of code for the given environment. Backups created on the Test and Live environments automatically checkout the [`git tag`](https://git-scm.com/book/en/v2/Git-Basics-Tagging)associated with the most recent deployment.

To restore the Dev environment using a backup from Test or Live, access the downloaded code archive in terminal and run:

```
git checkout -b tmp
git checkout master
git merge tmp
```

Include additional work and commit as needed, then use `git push origin master --force` to update the Dev environment on the same site or make an archive to import into a new site:

```php
# Specify the destination folder.
TARGET=~/Desktop
# Specify the source folder.
SOURCE=~/Projects/mysite
# Change directory to the source folder.
cd $SOURCE
# Create an archive
tar -czf $TARGET/code_archive_sitename.tar.gz .
```


## Import Your Code/Files/Database

1. Go to the Account page on [https://dashboard.pantheon.io/](https://dashboard.pantheon.io/).
2. Click **Create A New Site**.
3. Name your new site.
4. Choose **Import Archives**.
5. Select the **Provide separate code, database, and files archives** link.
6. In each of the fields, change the option from URL to File, then select the archives you previously downloaded.
7. Click **Import Site**.

The import process will create and deploy a new site based on the uploaded files. If there are issues, see [Migrate Sites to Pantheon](/docs/articles/sites/migrate) for possible solutions, or open a support ticket from your Dashboard. Be sure to include any error messages or relevant information.

## Additional Considerations
Retaining Git history, importing large file structures or databases:
The methods in this article will work well for small to medium sites, but will not import the Git repository commit history or logs. Also, Pantheon's import process cannot handle exceptionally large file structures or databases. For any of these scenarios, see [Migrate to Pantheon: Manual Site Import](/docs/articles/sites/migrate/manual-site-import).
