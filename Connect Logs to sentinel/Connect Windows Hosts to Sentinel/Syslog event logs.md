* After connecting the Sysmon agent to the windows machine, perform the following to enable Microsoft Sentinel to query the logs:

* *Azure portal -> Log analytics workspace -> select Legacy agents management in Settings area -> Add windows event log on windows event logs tab*
* *In the Add windows event log search box, enter: Microsoft-Windows-Sysmon/Operational. Sysmon isn't in the list by default*
* *Apply*

This can also be made from within Sentinel:
* *Settings > Workspace settings > Legacy agents management*

  ![image](https://github.com/AbhishekPratap9/Microsoft-Sentinel/assets/156197198/17e386d6-10bf-435d-af23-555b856be71d)

