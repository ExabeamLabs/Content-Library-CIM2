# Code Changes for microsoft-evterminalservices-xml-endpoint-notification-success-catchall (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_guid |  | ['Guid=(\'|")\{({process_guid}[^\}\'"]+?)\}(\'|")'] |
| edit_regex_field | process_id |  | ['<Execution ProcessID=(\'|")({process_id}\d+)(\'|") ThreadID=(\'|")({thread_id}\d+)(\'|")\/>'] |
| edit_regex_field | provider_name |  | ['<Provider Name=(\'|")({provider_name}[^\'"]+)(\'|")'] |
| edit_regex_field | thread_id |  | ['<Execution ProcessID=(\'|")({process_id}\d+)(\'|") ThreadID=(\'|")({thread_id}\d+)(\'|")\/>'] |
| edit_regex_field | user_sid |  | ['<Security UserID=(\'|")({user_sid}[^\'"]+)(\'|")\/>'] |