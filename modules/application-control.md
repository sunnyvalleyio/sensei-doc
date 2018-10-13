# Application Control

Sensei's Application Control engine uses "App DB" to understand and classify the application a particular connection packets carry. The database contains dynamic signatures which hint the packet engine to be able to classify the connections more accurately.  

{% hint style="info" %}
"APP DB" is maintained by Sunny Valley Networks. You can update it through [Status &gt; App DB Update & Reload](status.md#app-db-update-and-reload)
{% endhint %}

## Categorization

Applications are categorized by their type and listed in a click-to-open tree-view for convenient access.

![App Control settings](../.gitbook/assets/sensei-m5-app-controls-1.png)

## Dynamic Search

You can use dynamic search on top of the category list to filter out the items. We search as you type.

![Dynamic search helps you to filter](../.gitbook/assets/sensei-m5-app-controls-1-search.png)

## Blocking an Application or a Category

### Blocking an application 

Sensei allows you to block individual applications by clicking on the green check icons located on the left side of each application.

### Blocking an entire category

You can also block the entire category by clicking the green check icon located on the left side of the category name.

![](../.gitbook/assets/sensei-m5-app-controls-2.png)

### Activating the rules

When you're ok with the changes you made, click on the button lower right corner of the screen to save and activate the rules.

### Testing the results

The rules go in the action immediately after you hit the save button. The request silently blackholed on the user's end.

#### Testing MSN before the Ads blocked

![MSN homepage with ads](../.gitbook/assets/sensei-m5-app-controls-3-msn-before.png)

#### MSN Homepage after the Ads blocked by Sensei silently

![MSN homepage without ads](../.gitbook/assets/sensei-m5-app-controls-3-msn-after.png)



