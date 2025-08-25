# Code Changes for microsoft-evsecurity-xml-endpoint-domain-join-fail-16998 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_user_sid |  | ['<Data Name=(\'|")Computer Account SID:(\'|")>({dest_user_sid}[^<]+)<'] |
| edit_regex_field | event_name |  | ['EventData Name=(\'|")({event_name}[^>\'"]+)'] |
| edit_regex_field | process_id |  | ['<Execution ProcessID=(\'|")({process_id}\d+)(\'|") ThreadID=(\'|")({thread_id}\d+)(\'|")\/>'] |
| edit_regex_field | thread_id |  | ['<Execution ProcessID=(\'|")({process_id}\d+)(\'|") ThreadID=(\'|")({thread_id}\d+)(\'|")\/>'] |
| edit_regex_field | user_sid |  | ['<Security UserID=(\'|")({user_sid}[^\'"]+)(\'|")\/>'] |