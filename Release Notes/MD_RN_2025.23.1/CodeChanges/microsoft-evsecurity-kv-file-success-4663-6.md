# Code Changes for microsoft-evsecurity-kv-file-success-4663-6 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'access_mask', 'domain', 'event_code', 'event_name', 'file_dir', 'file_type', 'host', 'login_id', 'process_dir', 'process_name', 'process_path', 'src_file_ext', 'src_file_name', 'src_host', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['Computer(Name)? = "+({src_host}({host}[\w\-.]+))"'] |
| added_regex_field | src_host |  | ['Computer(Name)? = "+({src_host}({host}[\w\-.]+))"'] |
| removed_attribute | DupFields |  | N/A |