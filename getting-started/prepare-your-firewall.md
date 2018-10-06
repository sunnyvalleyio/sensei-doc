# Prepare Your Firewall

{% hint style="info" %}
Sensei is currently available for OPNsense open source firewall. This documentation based on OPNsense 18.1.x/18.7.x branches.
{% endhint %}

To install Sensei on your OPNsense firewall, you need to connect to it via `ssh` with `root` privileges.

1. Login to your OPNsense firewall's dashboard
2. Head to the `System > Settings > Administrations` menu
3. Enable all three checkboxes 
   1. Enable Secure Shell
   2. Permit root user login
   3. Permit password login

![](../.gitbook/assets/opnsense-admin-secure-shell-settings.png)



