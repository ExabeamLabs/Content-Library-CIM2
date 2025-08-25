# Code Changes for crowdstrike-falcon-cef-alert-trigger-success-host (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | alert_severity |  | ['({alert_severity}\d+)\|\s*(cat=|externalId=)', 'severityName=({alert_severity}[^\s]+)'] |