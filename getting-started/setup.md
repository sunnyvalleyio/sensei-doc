# Installing Sensei

This process is quite straight-forward and easy. You download an installer file onto the firewall and run it. Everything then gets taken care by the installer script.

{% hint style="info" %}
Sensei Community Edition is free-of-charge. You can download your copy from [https://www.sunnyvalley.io/sensei](https://www.sunnyvalley.io/sensei)  
{% endhint %}

## Connect to Your Firewall

```text
$ ssh root@your-firewall-ip
```

After a successful login, enter "8" as the option to drop to the shell

![Logging into OPNsense firewall via SSH](../.gitbook/assets/setup_2_ssh_to_your_firewall.png)

## Download Sensei Installer

Once you register your copy at [https://www.sunnyvalley.io/sensei](https://www.sunnyvalley.io/sensei), you'll be provided with a download URL to setup latest community edition. 

```text
root@fw:~ # fetch https://your-sensei-installer-script-url
```

![Downloading the installer script](../.gitbook/assets/setup_3_download_sensei.png)

## Run The Installer

After downloading your copy of setup script, run it with `sh` and approve with `y`

```text
root@fw:~ sh sensei_opnsense_installer.sh
Installing via OPNsense installer
Do you wish to install Sensei? y
```

Depending on your computer setup and your internet connection speed, it might take 2-4 minutes to complete.

Once the install completed, you can disconnect from your terminal, and disable your firewall's ssh service by unchecking the checkbox mentioned above.

## Initial Configuration Wizard

{% hint style="info" %}
To start using Sensei, first, you need to go through the Wizard which will guide you to start with the best initial configuration.
{% endhint %}

To start your "Initial Configuration Wizard"; 

* Login to your OPNsense Web UI
* Click Sensei from the left menu.
* Click on the Dashboard sub-menu. It will open up the Wizard.

#### 1- EULA

* Accept the End User Agreement.
* Click "Next" and get to the "Interface Selection" section.

#### 2- Interface Selection

* Select the Ethernet Interfaces to protect. To do that, click on an interface and use the right/left arrow buttons to move it to protected/unprotected interfaces combo box.
* Click "Next" and get to the "Security" section.

![Selecting Ethernet interfaces to protect](../.gitbook/assets/setup_5_eastpect_setup.png)

#### 3- Security

* Set your TCP Service password. This password protects the command line based CLI access to the packet engine. It is highly recommended to set this with a secure one.
* Click "Next" and get to the "Updates" .

#### 4- Updates

* Sensei uses OPNsense package system to deliver its updates. Configure the way you receive your Sensei updates as you feel convenient.



{% hint style="info" %}
Hands-on video: [https://www.youtube.com/watch?time\_continue=7&v=y6OE2FuzkF0](https://www.youtube.com/watch?time_continue=7&v=y6OE2FuzkF0)
{% endhint %}

