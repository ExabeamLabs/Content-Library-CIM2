# Code Changes for microsoft-defenderep-xml-report-create-success-1151 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | provider_guid |  | ['Guid\\*=(\'|")\{({provider_guid}[^}\']+)'] |
| edit_regex_field | user_sid |  | ['UserID\\*=(\'|")({user_sid}[^\'"]+)(\'|")'] |