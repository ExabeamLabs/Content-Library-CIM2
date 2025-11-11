# Code Changes for microsoft-sysmon-xml-process-close-5-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_guid |  | ['<Data Name\\*=(\'|")ProcessGuid(\'|")>\{({process_id}({process_guid}[^\}]+))'] |
| edit_regex_field | process_id |  | ['<Data Name\\*=(\'|")ProcessGuid(\'|")>\{({process_id}({process_guid}[^\}]+))', '<Data Name\\*=(\'|")ProcessId(\'|")>({process_id}.+?)<\/Data>'] |
| removed_attribute | DupFields |  | N/A |