# Changelog

## 0.8.0 - June 18, 2019

* **IPv6 Support** As promised - now Sensei has IPv6 support.
* **Virtio interface support** There were many requests that we make Sensei run on virtual interfaces like QEMU/KVM/Proxmox virtio. Sensei 0.8 combined with OPNsense 19.1.x new netmap enabled kernel, you can now run on virtio interfaces This is also a big enabler to run OPNsense and Sensei on most of the major Cloud and VPS operators. More info on that: [https://forum.opnsense.org/index.php?topic=11477.0](https://forum.opnsense.org/index.php?topic=11477.0)
* **Wireless interfaces support** Starting with OPNsense 19.1 and Sensei 0.8, you can now run Sensei on wireless interfaces.
* **VLAN interfaces support** Starting with OPNsense 19.1 and Sensei 0.8, you can now run Sensei on VLAN interfaces.
* **Better Cloud & Update Servers Availability**
* Users can now ignore the Hardware compatibility warning and install Sensei even if the HW resources are below what is advisable.
* You'll now get reported via an informative message in the UI if Sensei health check automatically stops Sensei service due to a HW resource shortage. Up until now, Sensei was doing this quite silently ;\)
* Number of Elasticsearch dependencies decreased by 1/3: faster installs & updates
* **Better Reporting**
* IPv6 reporting
* Ability to resolve local IP addresses to MDNS supplied hostnames
* Source Hostname is now the default instead of IP address in Session Reports \(IP is still available via a tooltip
* Ability to specify start and end times for Session Explorer Reports
* Ability to refresh Session Explorer Reports without having to close/re-open the report
* Mobile devices UI improvements

## 0.7.0 - December 26, 2018

* 350+ new applications identified.
* Google applications browsed via Chrome are now being identified \(QUIC over UDP protocol support\).
* Mobile browser compatibility: you can view reports from your mobile browser
* Reports enhancement: Data retirement option introduced. With this option you can define how long to keep your reports \(days\)
* Reports enhancement: Option to erase all reporting data
* Reports enhancement: Drill-down in Security reports is now available
* Reports enhancement: Daily executive reports. Selected reports delivered via a daily e-mail.
* You can easily add block/allow rules within Session Explorer based on Application and Application Category or SNI / hostname
* User's Manual in English.
* More deployment options for Home and Large scale users
* Changelog between updates
* Fixed Rebellion Theme compatibility issues.
* Better Cloud Nodes availability
* Better & smoother updates
* We speak your language now, we added i18n support to match your OPNsense UI language. English and German are there for now, more coming soon.
* Removed some large dependencies in preparation for embedded devices & PIE \(Position Independent Executable\) support.More performance & stability improvements.

