# Code Changes for microsoft-evsecurity-kv-service-create-success-4697-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_name', 'dest_host', 'domain', 'event_code', 'host', 'login_id', 'process_dir', 'process_name', 'process_path', 'service_name', 'service_type', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['\WComputer=({dest_host}({host}[\w\.\-]+))'] |
| added_regex_field | dest_host |  | ['\WComputer=({dest_host}({host}[\w\.\-]+))'] |
| removed_attribute | DupFields |  | N/A |