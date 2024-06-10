* There are three primary log types in Sentinel:
  * Analytics logs
  * Basic logs
  * Archive logs<br><br>

Data in each table in a Log Analytics workspace is retained for a specified period of time after which it's either removed or archived with a reduced retention fee.

* To access archived data, you must first retrieve data from it in an Analytics Logs table using one of the following methods:
  * Search jobs
  * Restore

![image](https://github.com/AbhishekPratap9/Microsoft-Sentinel/assets/156197198/bacc2670-aab0-41a4-8e72-e39f00faeb3e)<br><br>

* **Analytical Logs :**
  By default, all tables in a workspace are of type Analytics Logs, which are available to all features of a Log Analytics workspace and any other services that use the workspace.

* **Basic Logs :**
  You can configure certain tables as Basic Logs to reduce the cost of storing high-volume verbose logs you use for debugging, troubleshooting and auditing, but not for analytics and alerts. Tables configured for Basic Logs have a lower ingestion cost in exchange for reduced features. Basic logs are only retained for 8 days.<br>
  * KQL queries supported for Basic logs:
    * where
    * extend
    * project
    * project-away
    * project-keep
    * project-rename
    * project-reorder
    * parse
    * parse-where
  * KQL queries isn't supported:
    * join
    * union
    * aggregates (summarize)
  * _Table support :_
    * All tables in your Log Analytics are Analytics tables, by default. You can configure particular tables to use Basic Logs. You can't configure a table for Basic Logs if Azure Monitor relies on that table for specific features.<br>
    * You can currently configure the following tables for Basic Logs:
      * **All tables created with the Data Collection Rule (DCR)**-based custom logs API.
      * **ContainerLogV2**, which Container Insights uses and which include verbose text-based log records.
      * **AppTraces**, which contain freeform log records for application traces in Application Insights.
    * Configure log type/table retention:
      * Click log analytics
      * Select Tables tab
      * Select the Table
      * Select Manage table
      * Change Table plan, or retention period
      * Select SAVE

* **Archive Logs :**
  Archiving lets you keep older, less used data in your workspace at a reduced cost.<br>
  ![image](https://github.com/AbhishekPratap9/Microsoft-Sentinel/assets/156197198/baa80204-10af-460a-9912-644ce8bfb5d2)<br><br>
  During the interactive retention period, data is available for monitoring, troubleshooting and analytics. When you no longer use the logs, but still need to keep the data for compliance or occasional investigation, archive the logs to save costs. You can access archived data by running a search job or restoring archived logs.


