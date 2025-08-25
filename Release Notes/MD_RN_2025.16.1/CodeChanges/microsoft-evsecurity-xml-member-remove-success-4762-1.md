# Code Changes for microsoft-evsecurity-xml-member-remove-success-4762-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | member |  | ['<Data Name=(\'|")MemberName(\'|")>CN=({member}[^=]+?),CN=Users,'] |
| edit_regex_field | process_guid |  | ['Guid\\*=(\'|")\{({process_guid}[^\\'\}"]+)'] |
| edit_regex_field | provider_name |  | ['Provider Name\\*=(\'|")({provider_name}[^\\'"]+)'] |