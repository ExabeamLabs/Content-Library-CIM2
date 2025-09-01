# Code Changes for microsoft-evsecurity-xml-ds-replication-start-4932-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_dc |  | ['<Data Name\\*=(\'|")DestinationDRA(\'|")>.+?CN=({dest_dc}[^\s,]+)'] |
| edit_regex_field | dest_dra |  | ['<Data Name\\*=(\'|")DestinationDRA(\'|")>.+?CN=({dest_dra}[^<]+)'] |
| edit_regex_field | process_id |  | ['<Execution ProcessID\\*=(\'|")({process_id}\d+)'] |
| edit_regex_field | session_id |  | ['<Data Name\\*=(\'|")SessionID(\'|")>({session_id}\d+)<'] |
| edit_regex_field | src_dc |  | ['<Data Name\\*=(\'|")SourceDRA(\'|")>.+?CN=({src_dc}[^\s,]+)'] |
| edit_regex_field | src_dra |  | ['<Data Name\\*=(\'|")SourceDRA(\'|")>({src_dra}[^<]+)<'] |