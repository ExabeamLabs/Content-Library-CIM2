# Code Changes for microsoft-evsecurity-str-user-privilege-use-success-4674 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'dest_host', 'domain', 'event_code', 'host', 'login_id', 'object', 'object_server', 'object_type', 'privileges', 'process_dir', 'process_name', 'process_path', 'time', 'user'] |
| edit_regex_field | host |  | ['({dest_host}({host}[\w.\-]+)),特権のあるオブジェクトで操作が試行されました。'] |
| added_regex_field | dest_host |  | ['({dest_host}({host}[\w.\-]+)),特権のあるオブジェクトで操作が試行されました。'] |
| removed_attribute | DupFields |  | N/A |