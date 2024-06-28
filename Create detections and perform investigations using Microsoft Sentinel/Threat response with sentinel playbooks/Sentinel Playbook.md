### Deploy Sentinel
Create the Azure workspace
![image](https://github.com/AbhishekPratap9/Microsoft-Sentinel/assets/156197198/0fccc169-618e-4fa6-b2d5-cfe839eaa8f8)
### Check resources created 
* **Ap-sentinel** - Log Analytics workspace
* **NetworkWatcher_centralindia** - Network watcher
* **NetworkWatcher_polandcentral** - Network Watcher
* **SecurityInsights(Ap-sentinel)** - Solution
* **simple-vm** - Virtual Machine
* **simple-vmNetworkInterface** - Network Interface
* **st1d3vvqrwvxlnhs** - Storage account 
* **vnet1** - Virtual network

### Configure Connectors
1) Select Sentinel and desired workspace
2) *Select Sentinel -> select workspace created -> OVerview pane -> Content management -> Content Hub -> Azure Activity -> Install*
   ![image](https://github.com/AbhishekPratap9/Microsoft-Sentinel/assets/156197198/88b22613-a6eb-4f5f-a458-0801c5ccaf45)
3) *Sentinel -> Data connectors -> select Azure Activity -> open connectors page*
   ![image](https://github.com/AbhishekPratap9/Microsoft-Sentinel/assets/156197198/f4d965b8-1ec6-4dae-8a15-c3441a1ae74b)
4) *select Launch Azure policy Assignment Wizard*
    *Basic tab -> select subscription*<br>
    *Parameters -> select workspace*
    *Under Remediation tab -> select Create a remediation task -> Review + Create*
     ![image](https://github.com/AbhishekPratap9/Microsoft-Sentinel/assets/156197198/c6130054-551d-4fd3-9e3e-e307356c02e2)
     ![image](https://github.com/AbhishekPratap9/Microsoft-Sentinel/assets/156197198/a05dbfbd-1ee6-45ec-9319-86bfa05348f2)
     ![image](https://github.com/AbhishekPratap9/Microsoft-Sentinel/assets/156197198/3c802ab7-e126-4000-b4f9-9ed06bbd2b29)

     




    




