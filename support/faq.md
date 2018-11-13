# FAQ

## Which firewalls / network equipments are supported?

Our goal is to be able to run Sensei on any networking equipment \(firewalls, switches, UTMs\) which run on Layer 3-4. 

Currently the full integration has been completed for OPNsense open source firewall. ​This documentation is based on OPNsense 18.1.x/18.7.x branches.

## No Ethernet Interface is being shown in the Interface Configuration

If you cannot see any Ethernet Interfaces not being reported in the Configuration -&gt; Interface Selection menu, chances are that you're running on a virtualized environment like Promox/QEMU and you're using `VirtIO Ethernet`  . `Virtio Ethernet` and netmap does not play well together. As a workaround, we recommend using `Intel E1000` or `Realtek` as the network adapter type.

Please see below related answer:

## Can I run Sensei on a virtualized environment like Proxmox, VirtualBox, KVM?

Yes! However, be sure to avoid using `VirtIO Ethernet`. We recommend using `Intel E1000` or `Realtek` as the network adapter type.

You'll be able to use`VirtIO Ethernet` soon, when we finish our work on `netmap` \(the packet interface at FreeBSD\). We're sponsoring an effort to bring the latest netmap code to FreeBSD STABLE and CURRENT. This work will also involve a testing framework, originally developed for Google Summer of Code, and will ensure the stability of netmap infrastructure on FreeBSD during netmap code updates. 

## Are there any compatibility issues with OPNsense?

For OPNsense 18.1.x, we are aware of an issue where OPNsense upgrades might fail if you start OPNsense version updates while Sensei is running.

As a workaround, navigate to Sensei -&gt; Status and stop both Sensei and Elastic Search services before starting OPNsense firmware update.

If you're using OPNsense 18.7.x latest, you're good to go. The incompatibility has been fixed in upstream OPNsense code. 

## What is the correct hardware configuration?

Please refer to [Getting Ready section here](../getting-started/getting-ready.md#hardware-requirements-for-sensei).

## Does Sensei support IPv6?

IPv6 support is currently under development.

## Sensei does not recognize my Wi-Fi interface

We've been reported issues with Wi-fi drivers. Until addressed, Sensei filters out Wi-fi interfaces on the Interface Selection menu.

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

## Is Sensei open source?

Sensei is one of the first commercial software which is being made available for OPNsense platform.

Sensei consists of two modules:

* PHP / Python Scripts which provide the Web User Interface Functionality. **This part is open source.**
* The Packet Engine coded in C++, and **its source code is not open**.

## How do I get support?

Please refer to [Getting support section here](getting-support.md#community-edution-support)

## How much does Sensei cost?

Freemium Edition is forever free for OPNsense users.

There will be an upcoming Premium subscription with much more advanced features, which will be more suitable for more advanced use cases.

We'll announce the roadmap for both the commercial and community versions on our webpage at [https://www.sunnyvalley.io/sensei](https://www.sunnyvalley.io/sensei)



