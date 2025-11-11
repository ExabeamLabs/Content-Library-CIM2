# Code Changes for microsoft-evsecurity-kv-file-success-4663 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'additional_info', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'event_code', 'event_id', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'file_type', 'host', 'login_id', 'object', 'process_dir', 'process_name', 'process_path', 'result', 'src_host', 'time', 'user', 'user_sid'] |
| edit_regex_field | object |  | ['\WOBJECT_NAME\s*=\s*(null|({file_path}({object}[^\]]+?)))\s*\]'] |
| added_regex_field | file_path |  | ['\WOBJECT_NAME\s*=\s*(null|({file_path}({object}[^\]]+?)))\s*\]'] |
| removed_attribute | DupFields |  | N/A |