* The CEF Connector deploys a Syslog Forwarder server to support the communication between the appliance and Microsoft Sentinel.
* The server consists of a dedicated Linux machine with the Log Analytics agent for Linux installed.

![image](https://github.com/AbhishekPratap9/Microsoft-Sentinel/assets/156197198/8ddd38ba-3acc-4eef-9622-70c13eb30b2f)
 *The on-premises Syslog sources securely send events to an Azure Linux VM. The Linux VM with the Log Analytics agent installed then forwards the logs to the Microsoft Sentinel workspace* <br><br><br>

![image](https://github.com/AbhishekPratap9/Microsoft-Sentinel/assets/156197198/76c1ebfb-2799-4f4c-b5e2-d6e0946cae26)
*Alternatively, the following diagram displays the setup if you use a VM in another cloud or an on-premises machine. The on-premises Syslog sources securely send events to a Linux VM. The Linux VM with the Log Analytics agent installed then securely forwards the logs to the Microsoft Sentinel workspace*

### Security considerations
*Make sure to configure the machine's security according to your organization's security policy. For example, you can configure your network to align with your corporate network security policy and change the daemon's ports and protocols to align with your requirements.*
* Prerequisites
  * Make sure machine also meets the requirements.
  * Must have elevated permissions (sudo) on machine.
  * make sure software requirements are met(like python 2.7 or 3.0 is running) 

