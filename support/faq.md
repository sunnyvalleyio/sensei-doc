# FAQ

## Which open source firewalls are supported?

​Sensei is created to run on open source firewalls like OPNsense. This documentation based on OPNsense 18.1.x/18.7.x branches.

## Can I run Sensei on a virtualized environment like Proxmox, VirtualBox, KVM?

Yes! However, be sure to avoid using `VirtIO Ethernet`. We recommend using `Intel E1000` or `Realtek` as the network adapter type.

The reason is, `netmap` \(the packet interface at FreeBSD\) adds 12-byte headers for guest to host connections, and our application does not currently handle that. It is on our roadmap to address this.

## Are there any compatibility issues with OPNsense?

Currently, we are aware of an issue where OPNsense upgrades might fail if you start OPNsense version updates while Sensei is running.

We will be working this out with the OPNsense team.

As a workaround, navigate to Sensei -&gt; Status and stop both Sensei and Elastic Search services before starting OPNsense firmware update.

After that, you're good to go.

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
* The Packet Engine coded in C++, and its source code is not open to the public.

## How do I get support?

Please refer to [Getting support section here](getting-support.md#community-edution-support)

## How much does Sensei cost?

Community Edition is forever free for OPNsense users.

There will be an upcoming Enterprise edition with much more advanced features, which will be more suitable for more advanced use cases.

We'll announce the roadmap for both the commercial and community versions on our webpage at [https://www.sunnyvalley.io/sensei](https://www.sunnyvalley.io/sensei)



