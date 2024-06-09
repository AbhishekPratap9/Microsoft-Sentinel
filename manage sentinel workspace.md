Sentinel solution is installed in a Log Analytics Workspace. when creating a new Log Analytics Workspace is the region. The region specifies the location where the log data will reside.<br>
Three implementation options:
* Single-Tenant with single sentinel workspace
   central repository for logs across all resources within the same tenant.
   ![image](https://github.com/AbhishekPratap9/Microsoft-Sentinel/assets/156197198/692c6912-82be-47fb-ad64-febecf263b46)<br>

* Single-Tenant with regional Microsoft Sentinel workspace
  single-tenant with regional Microsoft Sentinel workspaces will have multiple Sentinel workspaces requiring the creation and configuration of multiple Microsoft Sentinel and Log Analytics workspaces.
  ![image](https://github.com/AbhishekPratap9/Microsoft-Sentinel/assets/156197198/02706bcc-c2c1-485f-b862-fe57a9c693f6)<br>
* Multi-Tenant workspace
  If you're required to manage a Microsoft Sentinel workspace, not in your tenant, you implement Multi-Tenant workspaces using Azure Lighthouse. This security configuration grants you access to the tenants. The tenant configuration within the tenant (regional or multi-regional) is the same consideration as before.
  ![image](https://github.com/AbhishekPratap9/Microsoft-Sentinel/assets/156197198/b397031e-3fd3-4a42-8e5e-570ab03ad092)



