# Code Changes for microsoft-evsecurity-sk4-share-access-5145-8 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'd_name', 'd_parent', 'dest_host', 'domain', 'event_code', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_type', 'host', 'login_id', 'result', 'share_name', 'share_path', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['"MachineName":"({dest_host}({host}[\w\-.]+))"'] |
| added_regex_field | dest_host |  | ['"MachineName":"({dest_host}({host}[\w\-.]+))"'] |
| removed_attribute | DupFields |  | N/A |