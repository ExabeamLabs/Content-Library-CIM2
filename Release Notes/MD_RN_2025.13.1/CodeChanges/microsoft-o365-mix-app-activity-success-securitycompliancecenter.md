# Code Changes for microsoft-o365-mix-app-activity-success-securitycompliancecenter (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | app |  | ['Workload"*:\s*"*({app}[^"]+)', 'destinationServiceName=({app}[^=]+?)\s+\w+=', 'exa_regex="Workload"*:\s*"*({app}[^"]+)', 'exa_regex=destinationServiceName=({app}[^=]+?)\s+\w+='] |