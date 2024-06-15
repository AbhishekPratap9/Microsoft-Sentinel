* The data connectors are included in out-of-the-box (OOTB), or built-in Content Hub solutions.
* We use Content Hub to install the solutions that include connectors.

### Content Hub
Once you've installed the Content Hub solutions, you can connect Microsoft and Azure-related services in the Data Connector page configuration section.<br>
* Office 365 connector:
  *  The Configuration option allows for the sending of Exchange, SharePoint, and Teams data. Based on your organization's specific needs, you can decide which data to ingest.
  *  The Data types show that all the data resides in the OfficeActivity table.

*  Microsoft Entra ID:
  *  two options for Sign-On logs and Audit logs
*  Entra ID Protection:
  * This connector sends data to the SecurityAlert table. The SecurityAlert table holds the alert data only without the underlying data that caused the alert
  * Create Incidents:  automatically creates an Incident based on and connected to the alert ingested to the SecurityAlert table from Microsoft Entra ID Protection. You can also activate the incident creation rule on the Analytics page.

* Azure Activity:
  *  Azure Activity Log is a subscription log that provides insight into subscription-level events that occur in Azure.
  *   Including events from Azure Resource Manager operational data, service health events, write operations taken on the resources in your subscription, and the status of activities performed in Azure.
