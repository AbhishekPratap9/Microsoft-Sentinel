* Windows Security Events via AMA connector uses Data Collection Rules(DCRs) to define the data to collect from each agent.<br>
Data collection rules offer you two distinct advantages:<br>
  * Manage collection settings at scale : independent of the workspace and independent of the virtual machine, which means they can be defined once and reused across machines and environments.
  * Build custom filters :  choose the exact events you want to ingest. The Azure Monitor Agent uses these rules to filter the data at the source and ingest only the events you want, while leaving everything else behind.

* **Pre-req:**
  * Must have Read & write permissions on Sentinel workspace
  * To collect events from any system that isn't an Azure virtual machine, the system must have Azure Arc installed and enabled before you enable the Azure Monitor Agent-based connector.
    * These resources include:
      * Windows servers installed on physical machines
      * Windows servers installed on on-premises virtual machines
      * Windows servers installed on virtual machines in non-Azure clouds

### Connect Windows Hosts:
* From Sentinel navigation menu, select *Data connectors*
* Select *Windows Security Events via AMA connector* from the list, and then select Open connector page on the details pane.
* Verify that you have the appropriate permissions as described under pre-req sections on the connector page.
* Under Configuration, select *+Add data collection rule*. The *Create data collection* rule wizard will open to right.
* Under *Basics*, enter a Rule name and specify a Subscription and Resource group where the data collection rule (DCR) will be created. This doesn't have to be the same resource group or subscription the monitored machines and their associations are in, as long as they are in the same tenant.
* In the *Resources tab*, select *+Add resource(s)* to add machines to which the Data Collection Rule will apply. *Select a scope dialog* will open, and you'll see a list of available subscriptions. Expand a subscription to see its resource groups, and expand a resource group to see the available machines. You'll see Azure virtual machines and Azure Arc-enabled servers in the list. You can mark the check boxes of subscriptions or resource groups to select all the machines they contain, or you can select individual machines. Select Apply when chosen all the machines. At the end of this process, the Azure Monitor Agent will be installed on any selected machines that don't already have it installed.
* On the Collect tab, choose the events you would like to collect. Select:
  * All security events
  * Common
  * Minimal
  * Custom
* *Review + Create* -> Validation passed -> select *create*

### X-path Query:
```
$XPath = '*[System[EventID=1035]]'
Get-WinEvent -LogName 'Application' -FilterXPath $XPath
```
If events are returned, the query is valid.
