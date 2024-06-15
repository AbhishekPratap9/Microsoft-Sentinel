Microsoft Defender XDR data connector provides alerts, incidents, and raw data from the Microsoft Defender XDR products including (but aren't limited to):
* Defender for Endpoint
* Defender for Identity
* Defender for Office 365
* Defender for Cloud Apps

### Azure Services 
The connectors for Microsoft and Azure-related services include<br>
* Entra ID
* Azure Activity
* Entra ID Protection
* Azure DDoS Protection
* Microsoft Defender for IoT
* Azure Information Protection
* Azure Firewall
* Microsoft Defender for Cloud
* Azure Web Application Firewall (WAF)
* Domain name server
* Office 365
* Windows firewall
* Security Events

### Vendor connectors & Connectors using Log Analytics API
* Sentinel provides an ever-growing list of vendor-specific data connectors. These connectors primarily use the CEF and Syslog connector as their foundation.
* Log Analytics Data Collector API to send log data to the Microsoft Sentinel Log Analytics workspace.

### Logstash plugin
Sentinel's output plugin for the Logstash data collection engine, you can send any log you want through Logstash directly to your Log Analytics workspace in Microsoft Sentinel.The logs are written to a custom table that you define using the output plugin.

### CEF and Syslog connector
* If there's no vendor-provided connector, you can use the generic Common Event Format(CEF) or Syslog Connector.
* Syslog is an event logging protocol that is common to Linux. Applications send messages that may be stored on the local machine or delivered to a Syslog collector.
* Common Event Format (CEF) is an industry-standard format on top of Syslog messages, used by many security vendors to allow event interoperability among different platforms.<br><br>
* **Syslog vs Common Event Format(CEF)**
  * CEF is always a superior choice because the log data is parsed into predefined fields in the CommonSecurityLog table. Syslog provides header fields, but the raw log message is stored in a field named SyslogMessage in the Syslog table. For the Syslog data to be queried, you need to write a parser to extract the specific fields.<br><br><br>

* **Connector Architecture Options:**
  * To connect the CEF or Syslog Collector to Sentinel, the agent must be deployed on a dedicated Azure virtual machine (VM) or an on-premises system to support the appliance's communication with Microsoft Sentinel. You can deploy the agent automatically or manually. Automatic deployment is only available if your dedicated machine is connected to Azure Arc or is a Virtual Machine in Azure.<br><br><br><br>

  
![image](https://github.com/AbhishekPratap9/Microsoft-Sentinel/assets/156197198/79c6e66e-6620-48a8-832c-d91b59769544)<br>
 following diagram illustrates on-premises systems sending Syslog data to a dedicated Azure VM running the Microsoft Sentinel agent.<br><br><br><br><br>
 ![image](https://github.com/AbhishekPratap9/Microsoft-Sentinel/assets/156197198/275bb3b8-0052-4521-b62f-d4164db5f274)<br>
  you can manually deploy the agent on an existing Azure VM, on a VM in another cloud, or an on-premises machine. The following diagram illustrates on-premises systems sending Syslog data to a dedicated on-premises system running the Sentinel agent.

### Connected Hosts
  The Data Connector page shows the connectors that are installed and can be filtered to show the ones with a Connected status. The count of Windows and Linux hosts connected with an agent is available in the Log Analytics workspace. To see your connected hosts do the following steps:

*Settings -> Workspace Settings(transfer to log analytics) -> Agents -> windows or Linux*
