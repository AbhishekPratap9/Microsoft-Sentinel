* *Designate and configure a Linux machine to forward the logs from your security solution to your Microsoft Sentinel workspace. This machine can be physical or virtual in your on-premises environment, an Azure VM, or a VM in another cloud*
* *run a script on the designated machine that performs the following tasks:*
  * *Installs the Log Analytics agent for Linux (also known as the OMS agent) and configures it for the following purposes:*
    * Listening for CEF messages from the built-in Linux Syslog daemon on TCP port 25226
    * Sending the messages securely over TLS to your Microsoft Sentinel workspace, where they're parsed and enriched
  * *Configures the built-in Linux Syslog daemon (rsyslog.d/syslog-ng) for the following purposes:*
    * Listening for Syslog messages from your security solutions on TCP port 514
    * Forwarding only the messages it identifies as CEF to the Log Analytics agent on localhost using TCP port 25226

### Run the deployment script:
To view the connector page:
* *select Data connectors -> select CEF -> select Open connector page on the preview pane -> verify the appropriate permissions -> Copy the "sudo wget …" command and run with elevated permissions on the dedicated Linux VM* <br><br>
![image](https://github.com/AbhishekPratap9/Microsoft-Sentinel/assets/156197198/19c093e1-de18-44cf-9423-88a8e249352f)

### Using the same machine to forward both plain Syslog and common event format messages
If you plan to use this log forwarder machine to forward Syslog messages as CEF, then to avoid the duplication of events to the Syslog and CommonSecurityLog tables:<br>

On each source machine that sends logs to the forwarder in CEF format, you must edit the Syslog configuration file to remove the facilities used to send CEF messages.


