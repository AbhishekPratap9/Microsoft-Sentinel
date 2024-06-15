* The Azure Activity Log is a subscription log that provides insight into subscription-level events that occur in Azure.
* The events included are from Azure Resource Manager operational data, service health events, write operations taken on the resources in your subscription, and the status of activities performed in Azure.
* The Azure Activity Data connector uses Azure Policy to apply an Azure Subscription log-streaming pipeline that sends the event data to Log Analytics.

### Deploy Azure Activity connector:
1) Scroll down to *Content management*, in sentinel left menu and Select *Content Hub*
2) In the Content Hub page, Search *Azure Activity* and select *Azure activity solution*
3) In the Azure Activity solution details pane, select *Install*
4) In *center Content column*, Select the *Azure Activity* Data connector<br>
  * This installs 12 Analytic rules, 14 Hunting queries, 1 workbook and Azure Activity Data connector
5) select *Open connector page*
6) In the *Instructions/Configuration area*, scroll down and under *connect your subscription*, select *Launch Azure Policy Assignment Wizard*
7) In the *Basics* tab, select *ellipsis* button (...) under *Scope* & select your *Azure subscription* from drop-down list and *select*
8) Select the *parameters* tab, choose your sentinel workspace from the *Primary Log Analytics workspace* drop-down list.
9) Select *Remediation* tab and select the *Create a remediation task* checkbox. This applies subscription configuration to send the information to the Log Analytics workspace.
10) Select *Review + Create* button to Review the configuration
11) Select Create to finish.
