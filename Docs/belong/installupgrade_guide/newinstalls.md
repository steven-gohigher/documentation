---
title: Belong - New Installations
breadcrumb: /belong:Belong/install_upgrade_guide:New Installations/

---

### First Steps

Before proceeding with any portion of the installation of Belong, please be sure to perform the following *First Steps*.

#### Gather Prerequisite Items

The following are required to have on hand prior to installing J!WHMCS Integrator

* Belong license key (accessed through your [Client Portal|https://client.gohigheris.com/clientarea.php] on our web site)
* Latest release of Dunamis Framework
* Latest release of Belong archive

#### Locate Your FTP Credentials

For the WHMCS portion of the product installation, you will need to have FTP access to upload files to your WHMCS application.  Please consult your hosting provider for more information on locating your FTP credentials.

#### Read Through The Installation Documentation

Please be sure to read through the documentation to see how it is supposed to be installed prior to performing any tasks.

### Upload and Activate Dunamis Framework for WHMCS

1. If you have not already done so, download the latest release of the [Dunamis Framework for WHMCS here|https://www.gohigheris.com/customer-downloads/dunamis-framework] (you must be signed in to do so).
2. Extract the *dunamis_whmcs_v{x.y.z}.zip* file to a folder on your local computer.  Contained within this archive are many files within two folders, an includes folder and a modules folder.
3. Using your favorite FTP program, upload the includes and modules folders to your WHMCS application.  You will notice that you have an includes and a modules folder already in place on your server where WHMCS is installed.  This is normal and expected.
4. Once the files have completely uploaded, log into the administrative back end of WHMCS using an account with sufficient privileges to activate and configure addon modules.
5. From the WHMCS Admin Home Screen, navigate to _Setup_ > _Addon Modules_.
6. Locate the _Dunamis Framework_ addon module in the list and click the _Activate_ button.
7. Once activated, click on the _Configure_ button and give your administrative account privileges to access the module.

### Upload Belong Addon Module for WHMCS

1. Extract the *belong_v{x.y.z}.zip* file to a folder on your local computer.  Contained within this archive are many files within a single folder called modules.
2. Using your favorite FTP program, upload the modules folder to your WHMCS application.  You will notice that you have a modules folder already in place on your server where WHMCS is installed.  This is normal and expected.
3. Once the files have completely uploaded, log into the administrative back end of WHMCS using an account with sufficient privileges to activate and configure addon modules.
4. From the WHMCS Admin Home Screen, navigate to _Setup_ > _Addon Modules_.
5. Locate the _Belong_ addon module in the list and click the _Activate_ button.
6. Once activated, click on the _Configure_ button and give your administrative account privileges to access the module.

### Install Belong Archive into Joomla!

1. Locate the *plg_system_belong_v{x.y.z}.zip* file that you downloaded from our site.  This one file contains the Belong System Plugin which handles all requests from Belong in WHMCS to Joomla.
2. Log into your Joomla backend using an account with Super User privileges.
3. Navigate to _Extensions_ > _Extension Manager_.
4. Under the_ Upload Package_ _File_ section click on the _Browse_ button and locate the plg_system_belong_v{x.y.z}.zip file you located in step 1.
5. Click on _Upload and Install_.
6. Joomla will now install and activate the Belong - System Plugin.

### Next Steps

After you have installed the product into your site, you are now read to configure the product.  Configuration must be done before your Joomla and WHMCS installations will work together.

* [Add or Change Your Belong License](Add or Change Your License)
* [Configuration Walk Through](http://)
* [Setup The Shared API Token](Setup the Shared API Token)
