# Code Changes for microsoft-azuremon-json-app-activity-success-runreadevent (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | full_name |  | ['"Identity":"\{\\*"UserName\\":\\*"({full_name}[^"\\]+)'] |
| edit_regex_field | object |  | ['"Identity":"\{[^\}]+\\*"UserObjectId\\":\\*"({object}[^"\\]+)"'] |