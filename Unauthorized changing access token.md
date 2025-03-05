# Prometheus Exporter for Jira(Lite)
Affected version: all

# Vulnerability Description
Any JIRA user can execute a request to POST /secure/PromForJiraSecureTokenConfigAction.jspa. This leads to a change in the plugin configuration, then the user can read the metrics because they know the token they set themselves (/prometheus/metrics?token=). 
This leads to a leak of sensitive information about the system.

# Impact
Vulnerability allows to unauthorized access to metrics that store for example users login.

# Discovered by
Michał Dziekan (https://www.linkedin.com/in/micha%C5%82-dziekan-8b77b91a2/)
