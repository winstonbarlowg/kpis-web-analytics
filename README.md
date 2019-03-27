# About

This repository should serve as a **template and playground** to get started with web tracking and analysis with Google Analytics and Google Tag Manager.
It is a learning material within PM_LU_38 - Web Analytics & KPIs, a learning unit at CODE University of Applied Sciences in Berlin. The course it taught by @Bolland

# Project setup

-  Register on Github.com if you haven't
-  [Clone](https://help.github.com/en/articles/cloning-a-repository) or [Fork](https://help.github.com/en/articles/fork-a-repo) this repository to your own Github account
-  This should download all files to your computer
-  Navigate to the downloaded folder using finder / explorer or your command line / terminal.
-  Folder structure: You'll find enumerated folders ('0-initial-setup', '1-event-tracking', etc.) that contain similar files and build upon each other.

# Learning steps

## 0-initial-setup

URL: [https://bolland.github.io/Web-Analytics-and-KPIs-for-beginners-template/0-initial-setup/index.html](https://bolland.github.io/Web-Analytics-and-KPIs-for-beginners-template/0-initial-setup/index.html)

This folder contains two basic pages with some dummy content. The goal here is to correctly set up Google Analytics tracking and publish the site on Github pages.

### Set up Google Analytics:

-  Create a [Google Analytics](https://analytics.google.com/) account
-  Retrieve your Google Analytics tracking code as explained [here](https://support.google.com/analytics/answer/1008080?visit_id=636885962702722888-2249578001&rd=1)
-  Add your tracking code in the `<head>` section of all html files
-  [Commit and push](https://stackoverflow.com/questions/2745076/what-are-the-differences-between-git-commit-and-git-push) your changes to your repository

### Publish the site to Github Pages

-  Enable your repository to use Github Pages (as explained [here](https://help.github.com/articles/configuring-a-publishing-source-for-github-pages/#enabling-github-pages-to-publish-your-site-from-master-or-gh-pages))
-  Your page should now run on your Github Pages and send tracking data to Google Analytics. You can check so by accessing the Real-time report in Google Analytics.

**Note:** you can also run the site on your **personal local or remote web server** instead of Github Pages.

## 1-event-tracking

[https://bolland.github.io/Web-Analytics-and-KPIs-for-beginners-template/1-event-tracking/index.html](https://bolland.github.io/Web-Analytics-and-KPIs-for-beginners-template/1-event-tracking/index.html)

Please only continue with this step once you have successfully finish setting up GA and the site in step 0.

This folder contains the same pages but adds **basic event tracking** to the buttons. Events triggered by clicking those buttons should appear in your Google Analytics view.

## 2-google-tag-manager

[https://bolland.github.io/Web-Analytics-and-KPIs-for-beginners-template/2-google-tag-manager/index.html](https://bolland.github.io/Web-Analytics-and-KPIs-for-beginners-template/2-google-tag-manager/index.html)

This folder builts upon the last two examples and shows implementation of **basic event tracking via 'datalayer.push'**.

To make this work:

-  Head over to [https://tagmanager.google.com/](Google Tag Manager) and create an account and container
-  Install the container on all pages in the folder (`index.html` and `learn-more.html`) like described [https://support.google.com/tagmanager/answer/6103696?hl=en](here)
-  Specify the events you want to track with `dataLayer.push()` in your code (examples in the files in this folder)
-  Verify that events are sent from Website -> Tag Manager with GTM's **preview mode**
-  Set up a **Google Analytics Pageview Tag** that is triggered on all pages
-  Set up a **Google Analytics Event Tag** that is triggered by the events you define with `dataLayer.push()`in your code.
-  Verify that events are sent from Tag Manager -> Google Analytics with GTM's **preview mode** or by looking at Google Analytics itself
