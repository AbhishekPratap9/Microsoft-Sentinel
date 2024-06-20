### Types of Analytics rules
search for potential threats by using the built-in analytics rules that Microsoft Sentinel Analytics provides, including the following types:
* **Anomaly** - Alerts are informational and identify anomalous behaviors<br><br>
* **Fusion** - Sentinel uses the Fusion correlation engine, with its scalable machine learning algorithms, to detect advanced multistage attacks.By default, Fusion detection is enabled in Microsoft Sentinel.<br>
At the time of writing this article, for Anomaly and Fusion detection, you must configure the following data connectors:
  * Out-of-the-box anomaly detections
  * Alerts from Microsoft Products
    * Microsoft Entra ID Protection
    * Microsoft Defender for Cloud
    * Microsoft Defender for IoT
    * Microsoft Defender XDR
    * Microsoft Defender for Cloud Apps
    * Microsoft Defender for Endpoint
    * Microsoft Defender for Identity
    * Microsoft Defender for Office 365

  * Alerts from scheduled analytics rules, both built-in and created by your security analysts. Analytics rules must contain kill-chain (tactics) and entity mapping information in order to be used by Fusion.
  * Some of the common attack detection scenarios that Fusion alerts identify include:
    * Data exfiltration
    * Data destruction
    * Denial of service
    * Lateral movement
    * Ransomware
* **Microsoft security** - Can configure Microsoft security solutions that are connected to Microsoft Sentinel to automatically create incidents from all alerts generated in the connected service.
  * You can configure the following security solutions to pass their alerts to Microsoft Sentinel:
    * Microsoft Defender for Cloud Apps
    * Microsoft Defender for Server
    * Microsoft Defender for IoT
    * Microsoft Defender for Identity
    * Microsoft Defender for Office 365
    * Microsoft Entra ID Protection
    * Microsoft Defender for Endpoint


* **Machine learning (ML) behavior analytics** - Sentinel Analytics includes built-in machine learning behavior analytics rules. You can't edit these built-in rules or review the rule settings.
* Scheduled alerts - Scheduled alerts analytics rules provide you with the highest level of customization. You can define your own expression using Kusto Query Language (KQL) to filter the security events, and you can set up a schedule for the rule to run.
* NRT (Near Real Time) rules
* Threat Intelligence

![image](https://github.com/AbhishekPratap9/Microsoft-Sentinel/assets/156197198/65876c00-e063-4585-a5af-ac229941a1d2)<br><br>


