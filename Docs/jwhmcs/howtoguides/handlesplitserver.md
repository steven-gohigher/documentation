---
title: J!WHMCS Integrator - How To Guide: Handling Split Server Installations
breadcrumb: /jwhmcs:J!WHMCS Integrator/howtoguides:How To Guides/handlesplitserver:Handling Split Server Installations/
 
---

### About Split Server Installations

Due to the complex nature of a Split Server Install, it is difficult to go into great detail concerning the steps to perform a split install, however if you must do a split install, these are the basic steps that must be performed.

#### What is a Split Server Installation?

A split server installation occurs when your Joomla application is located on one domain / subdomain and your WHMCS application is located at another domain / subdomain.  They both can physically be located in the same hosting account, but if they are on different domains or subdomains, this constitutes a split server install.

### Replicating Your Joomla Structure

If you have an SSL certificate installed on your WHMCS site but NOT on your Joomla site, this is by far the hardest portion of the install.  To start, you will want to visit your Joomla! web site and view the source code. If you have a caching plugin or optimization plugin active, you may need to disable it on your site if the cache file changes frequently (in theory it would not).

#### View Source Code

Upon viewing your source code, you will need to download all the media files that are used to render your Joomla! site.  Media files include the following file types:

* *Images* - all images including those declared in style sheets must be downloaded.
* *CSS* - Cascading Style Sheet files are required also to render your page properly.
* *Javascipt* - any javascript files necessary to render your site must also be copied.

Some of the most likely sources to find your media files include the following folders:

* *Template Directory* - This is the folder called /templates that contains the themed template you are using on your Joomla! site.
* *System Folders* - Some system folders such as /libraries or /system contain media that is used to render your Joomla! site.
* *Media Folders* - This folder is a common media folder used by components and modules to store images, stylesheets and javascripts
* *Images Folder* - Often designers will use the images folder to store images. Note that Joomla! also uses this folder for system content
* *Modules Folder* - Some modules have stylesheets or javascript files that are used to render specific modules.
* *Plugins Folder* - Some plugins have stylesheets or javascript files that are used to render specific content items
* *Components folder* - Some components have stylesheets or javascript files that are used to render component pages.

#### Download Media Files

You must download copies of the media files you identify in the source code to your computer. Any or all of the folders in Joomla! can contain media that must be downloaded. When you download them, *YOU MUST PRESERVE THE STRUCTURE!*

For instance, if you find a file in your /images/mycompany/ folder called 'logo.jpg', you must download it to your machine into a folder called /images/mycompany/. Sometimes the easiest thing to do is just download the whole site and then figure out locally what you don't need by deleting unnecessary folders.

#### Upload Media Files

With your media files downloaded to your local machine, you will now want to upload them to your WHMCS installation.  To do this, I recommend creating a folder in your WHMCS install called 'jwhmcs' or 'sitefiles' or something that you will be able to remember what the folder is there for as you don't want to delete it by accident.  Then upload the files to this folder in your WHMCS installation.  Remember to preserve the directory structures as you upload them.  This can take some time to complete depending on how many files you are working with.

### Configuring J!WHMCS Integrator

With the files uploaded to your site, the final step is to tell J!WHMCS Integrator where those files are so that the site will render properly.  To do this, follow these steps:

1. Log into the administrative back end of your WHMCS application using an account with access to the J!WHMCS Integrator addon.
2. Navigate to Addons > J!WHMCS Integrator.
3. Click on the Settings link beneath the J!WHMCS Integrator logo.
4. Click on Visual Integration on the left side which should bring up your settings for the visual integration of the site.
5. Locate the buttons for 'URL for Images / CSS / JS' and toggle it from 'Use Joomla URL' to 'Use Custom URL'.
6. In the field the appears below the toggle button, enter in your FQDN for WHMCS with the folder you used to upload the media files into.  For example, if your WHMCS is located at http://mydomain.com/whmcs and you uploaded the files to a folder called 'sitefiles', then you would enter http://mydomain.com/whmcs/sitefiles/
7. Click Save and you should be all set


Verify the site is now wrapping properly and secured.
