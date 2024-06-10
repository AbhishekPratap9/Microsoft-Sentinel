* For enabling sentinel contributor permission are required to the subscription and to use either reader or contributir is required.
### Configure Log analytics workspace:
  * if a existing log analytics workspace exist for the sentinel you are using, or create new workspace, after clicking on create log analytics we have to select 4 options:<br><br>
    Subscription : Select the subscription<br>
    Resource Group : Select or create a resource group<br>
    Name : Name of the log analytics workspace and will be the name of sentinel workspace<br>
    Region : Region where log data will be stored<br>


*  The Region is the location where ingested data is stored. The data location impacts data governance requirements. Workspaces can't move from region to region; you will need to recreate the workspace if the region option needs to be changed.
### Prompts
* Select create in the sentinel workspace, select the log analytics workspace as shown and then click add:
  ![image](https://github.com/AbhishekPratap9/Microsoft-Sentinel/assets/156197198/d7753590-0b6d-4b6c-a3ef-73fc975b0000)<br>
* After sentinel been added in the workspace, select the workspace to review the overall acenarion of the sentienl environmwnt.<br>
  ![image](https://github.com/AbhishekPratap9/Microsoft-Sentinel/assets/156197198/2d8da49c-9487-4695-90c7-d9f69e14afef)<br><br>
* **Create a watchlist:**
  * Click watchlist as shown and fill the info:<br>
  ![image](https://github.com/AbhishekPratap9/Microsoft-Sentinel/assets/156197198/f0c99e9c-f5ac-413b-ac8a-9ccdce572324)<br>
  * upload the file containing the host name.
  * Select the created watchlist and checlist it for enabling the current one.
  ![image](https://github.com/AbhishekPratap9/Microsoft-Sentinel/assets/156197198/9ec1098f-ce46-4bd2-870b-7b1192e7067b)<br>
  * View logs
  ![image](https://github.com/AbhishekPratap9/Microsoft-Sentinel/assets/156197198/1322ec42-4ac3-49f7-b89d-20c51be15f69)<br><br>
* **Threat Intelligence:**
  * In the threat intelligence, select Add-new and fill the details as shown:
    ![image](https://github.com/AbhishekPratap9/Microsoft-Sentinel/assets/156197198/85009577-6a2e-449f-b4a2-3ca127bbc934)
  * In the logs column, type the quesry for log showing the threat:
    ![image](https://github.com/AbhishekPratap9/Microsoft-Sentinel/assets/156197198/75bf13c7-d99e-4278-9c1f-937a90a5fdac)<br><br>
* **Log retention:**
  * In the left pane, select settings in the configuration menu<br>
    ![image](https://github.com/AbhishekPratap9/Microsoft-Sentinel/assets/156197198/cc34ed53-af70-45bf-bcd4-c1dacd184911)
  * Select workspace settings<br>
    ![image](https://github.com/AbhishekPratap9/Microsoft-Sentinel/assets/156197198/9dc849e7-4f47-4e28-9150-4a10e88b609c)
  * Select Tables, after clicking workspace settings<br>
    ![image](https://github.com/AbhishekPratap9/Microsoft-Sentinel/assets/156197198/ce1e88a2-0379-4110-bd88-dc4f75c2adfb)<br>
  * Select manage tables by clciking the ellipsis<br>
    ![image](https://github.com/AbhishekPratap9/Microsoft-Sentinel/assets/156197198/569f4039-c1f7-464c-bf18-04a7503e7cfc)
  * Select the swecurity event and then set the total retention period as 180 days
    ![image](https://github.com/AbhishekPratap9/Microsoft-Sentinel/assets/156197198/a4f9f680-d23d-4358-b336-76f6f3cbec4e)







  





