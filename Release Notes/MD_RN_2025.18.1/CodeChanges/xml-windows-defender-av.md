# Code Changes for xml-windows-defender-av (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | provider_guid |  | ['Guid\\*=(\'|")\{({provider_guid}[^}\']+)'] |
| edit_regex_field | user_sid |  | ['UserID\\*=(\'|")({user_sid}[^\'"]+)(\'|")'] |