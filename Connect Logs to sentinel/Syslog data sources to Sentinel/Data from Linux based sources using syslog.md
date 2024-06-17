### Azure Linux VM
1) *Azure portal -> Monitor (in search bar) -> Data colection rules (in settings of monitor section) -> select Create*
   ![image](https://github.com/AbhishekPratap9/Microsoft-Sentinel/assets/156197198/6e4eb54e-4631-45be-9594-94c8b0232fbe)<br><br>
2) *In the Data collection Rule Basics tab, Enter Rule name and specify Subscription, Resource Group, Platform Type (select Linux)*
3) *select Next:Resources*
4) *On Data collection Rule Resources tab, select + Add resources*
5) *In Select a scope page ,expand the Scope column for subscription and Resource group types until target VM is displayed*
6) *Select target VM and select Apply. Your Linux VM displayed as a Resource*
   ![image](https://github.com/AbhishekPratap9/Microsoft-Sentinel/assets/156197198/4a5b4d11-d580-4594-a358-afad7ab4bdb2)
7) *Next: Collect and deliver*
8) *Data Collection Rule, Collect and deliver tab, select + Add data source*
9) *In Add data source page, select Linux Syslog from the Data source type drop-down menu, Select Add data source*
10) *Review + create, (Create after Validation passed is diplayed)*
> This process initiates the Azure Monitor Linux Agent extension install.

11) *Locate Virtual machines and select Linux VM as a Data collection Rule resource*
12) *On Virtual machine Overview, scroll to the Settings section and select Extensions + applications*
13) *Under Extensions tab, You should see AzureMonitorLinuxAgent displayed*
    ![image](https://github.com/AbhishekPratap9/Microsoft-Sentinel/assets/156197198/8153e4a8-77a8-4c3a-8642-de1b644b9ed0)
> If Defender for Cloud Auto-provisioning is enabled, the Azure Monitor Linux Agent will be installed by default as an extension using Azure Policy assignment.

### For other Linux machine
To install the agent on non-Azure Linux physical or virtual machines:
1) *Azure portal -> enter **Arc** in search resources search bar -> Azure Arc -> **Servers** -> IN the servers page, select **+ Add***
2) *On the **Add servers with Azure Arc** page, locate **Add a single server box** -> **Generate script** also on the same page -> **Prerequisites** tab, review and **Next***
3) *on the **Add servers with Azure Arc** page, select the Resource Group, Region and then select **Linux for OS**, Set connectivity methods, CLick **NEXT***
   ![image](https://github.com/AbhishekPratap9/Microsoft-Sentinel/assets/156197198/a69c6108-5659-404a-8d8e-6bae51f3b71c)



