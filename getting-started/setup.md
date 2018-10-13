---
description: How to install Sensei with a one-liner command
---

# Installing Sensei

Installing Sensei is straight-forward and easy. You just run a one-liner shell command to download the installer and run it. That's it, everything then gets taken care by Sensei.

{% hint style="info" %}
Sensei Community Edition is forever free-of-charge. We strongly recommend you register to keep in touch with updates and new features. You can register here: [https://www.sunnyvalley.io/sensei](https://www.sunnyvalley.io/sensei)  
{% endhint %}

## Connect to Your Firewall

```text
$ ssh root@your-firewall-ip
```

After a successful login, enter "8" as the option to drop to the shell

![Logging into OPNsense firewall via SSH](../.gitbook/assets/opnsense-terminal-1.png)

## Download & Run Sensei Installer

Run the following one-liner command to download and invoke the installer script. 

```text
root@fw:~ # curl https://updates.sunnyvalley.io/getsensei | sh
```

![Downloading and running the Sensei installer](../.gitbook/assets/opnsense-terminal-3-getsensei-1.png)

Hence we passed the downloaded script to `sh`, it will automatically run the installer script.

```text
Installing via OPNsense installer
Do you wish to install Sensei? y
```

Install script will copy the installation files onto the filesystem and will add a menu item within the Firewall Web User Interface. 

Depending on your computer setup and your internet connection speed, it might take 1-4 minutes to complete.

{% hint style="info" %}
You can get detailed info about suggested hardware on [Getting Started &gt; Hardware Requirements​](getting-ready.md).
{% endhint %}

![InstInstalling Sensei](../.gitbook/assets/opnsense-terminal-3-getsensei-2.png)

Once the install is completed, you can disconnect from your terminal, and disable your firewall's ssh service by unchecking the checkboxes mentioned above.

## Initial Configuration Wizard

{% hint style="info" %}
To start using Sensei, first, you need to go through the Wizard which will guide you to start with the best initial configuration.
{% endhint %}

To start your "Initial Configuration Wizard"; 

* Log in to your OPNsense Web UI,
* Click Sensei from the left menu,
* Click on the Dashboard sub-menu. It will open up the Wizard.

### 1- EULA

* Accept the End User License Agreement \(Scroll & read the terms to get to the next button\).
* Click "Next" and get to the "Interface Selection" section.

![](../.gitbook/assets/sensei-0-wizard-tab1-welcome-1.png)

### 2- Interface Selection

* Select the Ethernet Interfaces to protect. To do that, click on an interface and use the right/left arrow buttons to move it to protected/unprotected interfaces combo box.
* Click "Next" and get to the "Cloud Reputation" section.

![](../.gitbook/assets/sensei-0-wizard-tab2-interface-selection-2.png)

### 3- Cloud Reputation

The Cloud Threat Intelligence data is queried real time when anyone makes a connection through your network. It enables us to respond to malware and wireless outbreaks in real time and very fast.

The engine processes the request, queries to "SVN Cloud" in real-time and decides whether it will be blocked or allowed. We check against 140+ Million Websites, under 120+ categories in milliseconds.

Cloud Threat Intel settings let you;

* Enable/Disable the cloud reputation & web categorization engine
* Set local domain settings to be excluded from cloud queries

![](../.gitbook/assets/sensei-0-wizard-tab3-cloud-reputation-2.png)

### 4- Sensei CLI \(Security\)

* Set your TCP Service password. This password protects the command line based CLI access to the packet engine. It is highly recommended to set this with a secure one.
* Click "Next" and get to the "Updates" .

![](../.gitbook/assets/sensei-0-wizard-tab4-sensei-cli.png)

### 5- Updates & Health Check

{% hint style="info" %}
Sensei uses OPNsense package system to deliver its updates. Configure the way you receive your Sensei updates as you feel convenient.
{% endhint %}

* **Self Health Check:** If enabled, "Self Health Check" monitors the system's memory, CPU, disk usage and core services if they're working correctly, and raises alerts if anything goes wrong. Self Health Check also stops the relevant services if they're consuming excessive system resources.
* **Check for Updates Automatically:** Checks automatically for the updates and creates a notification on the status page.
* **Update Databases and Threat Intelligence Data Automatically:** Checks automatically for the updates and creates a notification on the status page .
* **Enable Generation of Support Data:** If enabled, Sensei collects supporting data during unusual events and crashes. You can share this data while opening a ticket with us. 

![](../.gitbook/assets/sensei-0-wizard-tab5-updates-health-check.png)

### 6- Deployment Size

Sensei supports up to 1000 concurrent users on an everyday PC. You can set your Sensei installation's capacity here.

{% hint style="info" %}
You can get detailed info about suggested hardware on [Getting Started &gt; Hardware Requirements​](getting-ready.md)
{% endhint %}

![](../.gitbook/assets/sensei-0-wizard-tab6-deployment-size-1.png)

### 7- Finish

Click the Finish button to save your initial configuration data and start using Sensei.

![](../.gitbook/assets/sensei-0-wizard-tab7-finish-1.png)

## Hands-on Video

{% hint style="info" %}
Hands-on video: [https://www.youtube.com/watch?time\_continue=7&v=y6OE2FuzkF0](https://www.youtube.com/watch?time_continue=7&v=y6OE2FuzkF0)
{% endhint %}

{% embed url="https://www.youtube.com/watch?time\_continue=7&v=y6OE2FuzkF0​" %}

