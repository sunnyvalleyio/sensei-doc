# FAQ

## Is Sensei open source?

Sensei consists of two modules:

* The Packet Engine coded in C++. **This part is closed source**.
* PHP Code & Python Scripts which provide the Web User Interface Functionality. **This part is open source.**

## Which firewalls / network equipments are supported?

Our goal is to be able to run Sensei on any networking environment; be it a container, cloud, virtual or bare-metal deployment \(firewalls, switches, UTMs\) which processes Layer 3-4 traffic. 

Currently the full integration has been completed for OPNsense open source firewall. ​This documentation is based on OPNsense 19.1.x/18.7.x/18.1.x branches.

## No Ethernet Interface is being shown in the Interface Configuration

If you cannot see any Ethernet Interfaces not being reported in the Configuration -&gt; Interface Selection menu, chances are that you're running on a virtualized environment like Promox/QEMU and you're using `VirtIO Ethernet`  . `Virtio Ethernet` and netmap does not play well together. As a workaround, we recommend using `Intel E1000` or `Realtek` as the network adapter type.

Please see below related answer:

## Can I run Sensei on a virtualized environment like Proxmox, VirtualBox, KVM?

Yes! However, if you're using Sensei 0.7.x release, be sure to avoid using `VirtIO Ethernet`. We recommend using `Intel E1000` or `Realtek` as the network adapter type.

**Starting with Sensei 0.8.0 OPNsense 19.1.x, you'll be able to use`VirtIO Ethernet`** 

This set includes a work on `netmap` \(the packet interface at FreeBSD\). We've sponsored an effort to bring the latest netmap code to FreeBSD STABLE and CURRENT. This work also involves a testing framework, originally developed for Google Summer of Code, and ensures the stability of netmap infrastructure on FreeBSD during netmap code updates. 

## Are there any compatibility issues with OPNsense?

If you're using OPNsense 18.7.x/19.1.x latest, you should be good to go. 

For OPNsense 18.1.x, we are aware of an issue where OPNsense upgrades might fail if you start OPNsense version updates while Sensei is running.

As a workaround, navigate to Sensei -&gt; Status and stop both Sensei and Elastic Search services before starting OPNsense firmware update.



## What is the correct hardware configuration?

Please refer to [Getting Ready section here](../getting-started/getting-ready.md#hardware-requirements-for-sensei).

## Does Sensei support IPv6?

Yes

## Sensei does not recognize my Wi-Fi interface

Starting with 0.8.0 beta1 and OPNsense 19.1.x, you can now protect wi-fi interfaces. 

## Reports: some charts are broken

This is because of  broken Elasticsearch indices. This happens when there is an unexpected power loss on the firewall .e.g. an electricity outage, abnormal shutdown of the firewall etc. Elasticsearch does a lot of buffering, writing the buffers to the indices from some time to time. If a partial write is in place than chances are high that your indices might get corrupt. 

**Solution:** Go to Sensei -&gt; Configuration -&gt; Reporting & Data. Click "Perform health check for indices". It'll take care of the rest for you.

## How do I reset to factory defaults?

* Navigate to `Sensei > Configuration`
* Click on Uninstall tab
* Click on "`Reset to factory defaults`" button. 

When you click on any Sensei submenu, you'll be redirected to the initial Configuration Wizard to start over.

## How do I uninstall the plugin?

* Navigate to `Sensei > Configuration`
* Click on "`Uninstall`" tab
* Click on "`Uninstall Sensei packet engine`" button.
* Confirm that you want to proceed.

## How do I get support?

Please refer to [Getting support section here](getting-support.md#community-edution-support)

## How much does Sensei cost?

Freemium Edition is forever free for OPNsense users.

There will be an upcoming Premium subscription with much more advanced features, which will be more suitable for more advanced use cases.

Details about the premium subscription will be announced in July 2019.

We'll announce the roadmap for both the commercial and community versions on our webpage at [https://www.sunnyvalley.io/sensei](https://www.sunnyvalley.io/sensei)



