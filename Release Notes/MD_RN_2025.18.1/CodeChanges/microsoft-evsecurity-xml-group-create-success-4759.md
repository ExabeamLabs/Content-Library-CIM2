# Code Changes for microsoft-evsecurity-xml-group-create-success-4759 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_guid |  | ['Guid\\*=(\'|")\{({process_guid}[^\\'\}]+)'] |