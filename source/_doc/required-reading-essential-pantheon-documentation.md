---
title: Required Reading: Essential Pantheon Documentation
description: Recommended documentation to learn about Pantheon Website Management Platform's technologies.
categories:
  - getting-started
keywords: getting started, get started, pantheon, best practices,
---
Pantheon is not web hosting. It is a highly-tuned, distributed, and instantly scalable web platform. Pantheon also integrates development best practices and tools into the platform, to get the developer back to writing code, not configuring servers and carrying pagers.

Our tech includes nginx, PHP, Redis, Varnish, Solr and Git&mdash;common tools in web development. You don't have to configure them, but an understanding of how they interact with your applications on Pantheon is important. Review the following must-read list to ensure developer success.

## Get to Know Pantheon

- [Getting Started](/docs/getting-started)  
- [Using the Pantheon Workflow](/docs/using-the-pantheon-workflow/)
- [All About Application Containers](/docs/all-about-application-containers/)
- [Platform Considerations](/docs/platform-considerations/)  
- [Enable Secure HTTPS Communication](/docs/adding-a-ssl-certificate-for-secure-https-communication)
<div class="alert alert-info">
<h4>Note</h4>
Pantheon containers spin down after ~1 hour of idle time. Live environments on a paid plan will spin down after 12 hours of idle time. On receiving a web request, they are spun up, usually within 30 seconds. If you try to connect to the database, you may experience an error. Load the home page, and you can connect.
</div>
## Build
- [Migrate Sites to Pantheon](/docs/)  
- [rsync and SFTP](/docs/rsync-and-sftp)
- [Configuring settings.php](/docs//configuring-settings-php) or [Configuring wp-config.php](/docs/configuring-wp-config-php)
- [Drupal Drush Command-Line Utility](/docs/drupal-drush-command-line-utility)
- [Cron for WordPress](/docs/cron-for-wordpress) or [Cron for Drupal](/docs//cron)

## Launch
- [Going Live](/docs/going-live/)
- [Domains and DNS](/docs/domains)
## Run
- [Optimization for Pantheon and the Cloud](/docs/optimizing)
- [New Relic Performance Analysis on Pantheon](/docs/new-relic-performance-analysis)
- [Applying Upstream Updates](/docs/applying-upstream-updates)
- [Varnish Caching for High Performance with Drupal and WordPress](/docs/varnish)
- [Redis as a Caching Backend](/docs/redis-as-a-caching-backend)
- [Drupal 7 Performance and Varnish Caching Settings](/docs//drupal-performance-and-caching-settings)
- [Content Delivery Network (CDN) for File Distribution](/docs//content-delivery-network-cdn-for-file-distribution/)
- [SSO and Identity Federation on Pantheon](/docs/sso-and-identity-federation/)
- [Backup Creation](/docs/backup-creation)

## Debug

- [PHP Errors and Exceptions](/docs/php-errors-and-exceptions/)
- [Errors and Server Responses](/docs/errors-and-server-responses/)

## Support

- [Scope of Support](/docs/scope-of-support/)
- [Getting Support](/docs/getting-support)
