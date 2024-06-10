* Sentinel watchlists enable collecting data from external data sources for correlation with the events in your Microsoft Sentinel environment. Once created, you can use watchlists in your search, detection rules, threat hunting, and response playbooks. * Watchlists are stored in your Microsoft Sentinel workspace as name-value pairs and are cached for optimal query performance
* Watchlists can be used as:
  * Investigating threats and responding to incidents quickly with the rapid import of IP addresses, file hashes, and other data from CSV files.
  * Importing business data as a watchlist.
  * Reducing alert fatigue. Create allowlists to suppress alerts from a group of users, such as users from authorized IP addresses that perform tasks that would normally trigger the alert, and prevent benign events from becoming alerts.
  * Enriching event data. Use watchlists to enrich your event data with name-value combinations derived from external data sources.

### Create a watchlist
1) Go to Microsoft Sentinel > Configuration > Watchlist and select Add new.
2) On the General page, provide the name, description, and alias for the watchlist, then select Next.
3) On the Source page, select the dataset type, upload a file, then select Next.
4) Next, review the information, verify that it's correct, then select Create. A notification appears once the watchlist is ready.
