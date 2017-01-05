---
Topics: PHP
Keywords: log;logging;debug;troubleshoot;trouble shoot;error;diagnose;
Question: How do I enable PHP logging Answer
---
# How can I enable PHP logging to troubleshoot PHP issues?
1. Log into KUDU website at https://<yourwebsitename>.scm.azurewebsites.net
2. In the top menu select Debug Console | CMD
3. Click on Site folder
4. Click on wwwroot folder
5. Click on + icon and New File
6. Set the file name as .user.ini
7. Click on the pencil icon next to .user.ini
8. Add this text log_errors=on
9. Click save button
10. Next, click on pencil icon next to wp-config.php
11. Change the text as shown below
```
//Enable WP_DEBUG modedefine('WP_DEBUG', true);
//Enable Debug Logging to /wp-content/debug.logdefine('WP_DEBUG_LOG', true);
//Supress errors and warnings to screendefine('WP_DEBUG_DISPLAY', false);
//Supress PHP errors to screenini_set('display_errors', 0);
```
12.Restart your web app from the web app menu in Azure Portal.

For more details please click [here](https://github.com/prashanthmadi/QAmaker/tree/master/opensource/php)
