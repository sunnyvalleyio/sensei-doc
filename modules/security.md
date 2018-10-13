---
description: Sensei Security
---

# Security

Sensei is developed in a way to give all the controls at your hands. To achieve this, we thrived our best to make almost everything configurable. On the Security screen, you can set your general policy of how threat analysis will work and set the rest on the App Control and Web Control modules.

{% hint style="info" %}
The engine processes the request, queries to "SVN Cloud" in real-time and decides whether it will be blocked or allowed. We check against 140+ Million Websites, under 120+ categories in milliseconds.
{% endhint %}

The Cloud Threat Intelligence data is queried real-time when any connection attempt is made through your network. It allows us to respond to malware and wireless outbreaks in real time and very fast.

![Sensei: Security Control Settings](../.gitbook/assets/sensei-m4-security.png)

### Block Domain Parking Sites

Parked domains are web pages typically with a single page with ads. They do not provide any value to the user. They are used by legitimate domain registrars to monetize the visits of users who land on the main page.

On the other hand, parked domains can also host suspicious and / or malicious content, especially when used by an Ad provider. Ad providers are known to be leveraged by cyber criminals to serve malvertisements. 

What's more, landing pages of parked domains are known to serve malware on a large scale. 

### Block Empty or Under Construction Sites

These sites are valid web sites but with a single page which denotes it is under construction or empty. Like parked domains, and because these sites are typically not maintained well, these sites are again the target of cyber criminals. After breaking into these sites, cyber criminals deploy scripts to distribute their malicious software from these sites. 

### Block Hacking Sites

Block sites which distribute hacking related content. 

### Block Malware Activity

Block sites that are known to host malware.

### Block Phishing Servers

Block sites that are known to host malicious software being used by phishing campaigns. 

### Block Potentially Dangerous Sites

Block sites that are potentially dangerous. Those are the sites that we're not %100 sure that they are malicious but they are displaying suspicious activity which resembles a malicious site. 

### Block Remote Access Tools

Block Remote Access Tools, that might be leveraged by malicious software to communicate with their Command and Control Centers. 

### Block Spam Sites

Block sites which distribute spam. 

### Block Warez Sites

Block Warez sites. 

### Block Undecided and Not Safe Sites

Undecided sites are the sites that our Web Categorization Service heard of but have not come to a decision yet. They have been processed at least once by our AI based Web Categorization service, but has not been categorized yet. 

Undecided Not Safe sites are the subset of these sites that we suspect of a malicious activity. 

### Block Decided and Not Safe Sites

Decided Not Safe sites are the subset of the categorized sites that we suspect of a malicious activity.

### Block Undecided Sites

Undecided sites are the sites that our Web Categorization Service heard of but have not come to a decision yet. They have been processed at least once by our AI based Web Categorization service, but has not been categorized yet. 

You can block all sites that are awaiting for being re-classification by clicking this option.

### Block Unknown Sites

Unknown sites are the sites our Web Categorization engine did not hear before. We did not even know that they existed. 

You can block all sites that are unknown to us by clicking this option.

{% hint style="info" %}
When we see a **Unknown Site** for the first time, it is immediately being queued for processing by our _AI based classification system_. 

AI based classification system tries to classify it. If there is success, the web category is immediately updated and in one hour, this new information is propagated to the entire Cloud Web Categorization & Threat Intelligence System. 

If the AI based classification cannot classify the web site, it is marked as **"Undecided"**, and queued again for a later processing. 
{% endhint %}

