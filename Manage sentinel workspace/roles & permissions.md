Microsoft Sentinel uses Azure **role-based access control (RBAC)** to provide built-in roles that can be assigned to users, groups, and services in Azure.<br>
* Microsoft Sentinel-specific roles:
  * _Microsoft Sentinel Reader_ : can view data, incidents, workbooks, and other Microsoft Sentinel resources.
  * _Microsoft Sentinel Responder_ : can, in addition to the above, manage incidents (assign, dismiss, etc.)
  * _Microsoft Sentinel Contributor_ : can, in addition to the above, create and edit workbooks, analytics rules, and other Microsoft Sentinel resources.
  * _Microsoft Sentinel Automation Contributor_ : allows Microsoft Sentinel to add playbooks to automation rules. It isn't meant for user accounts.
* Additional roles and permissions:
  * _Working with playbooks to automate responses to threats_ :  might want to assign to specific members of your security operations team the ability to use Logic Apps for Security Orchestration, Automation, and Response (SOAR) operations. **You can use the Logic App Contributor role to assign explicit permission for using playbooks**.
  * _Permissions to sentinel to run playbooks_ :  To grant these permissions to this service account, your account must have Owner permissions on the resource groups containing the playbooks.
  * _Connecting data sources to Microsoft Sentinel_ : For a user to add data connectors, you must assign the user write permissions on the Microsoft Sentinel workspace. Also, note the required other permissions for each connector, as listed on the relevant connector page.
  * _Guest users assigning incidents_ :  in addition to the Sentinel **Responder role**, the user will also need to be assigned the role of **Directory Reader**.
  * _Creating and deleting workbooks_ : create and delete a Sentinel workbook, the user requires either the Sentinel **Contributor role** or a lesser Sentinel role plus the Azure Monitor role of Workbook Contributor.
