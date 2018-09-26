# Prepare Your Firewall

To install Sensei on your open source firewall, you need to connect to it via `ssh` with `root` privileges.

{% hint style="info" %}
Sensei is created to run on open source firewalls like pfSense, OPNsense, etc. This setup documentation based on OPNsense 18.1.x/18.7.x branches.
{% endhint %}

1. Login to your OPNsense firewall's dashboard
2. Head to the System &gt; Settings &gt; Administrations menu
3. Enable all three checkboxes 

![Enabling SSH access on OPNsense](../.gitbook/assets/setup_1_opnsense_enable_ssh.png)
