# Code Changes for microsoft-evsecurity-xml-configuration-modify-success-4950 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_host', 'event_code', 'host', 'process_id', 'result', 'run_level', 'thread_id', 'time'] |
| edit_regex_field | host |  | ['<Computer>({dest_host}({host}[\w\-.]+))</Computer>'] |
| added_regex_field | dest_host |  | ['<Computer>({dest_host}({host}[\w\-.]+))</Computer>'] |
| removed_attribute | DupFields |  | N/A |