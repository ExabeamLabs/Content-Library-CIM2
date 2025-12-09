# Code Changes for microsoft-evsecurity-kv-share-access-success-5140 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'additional_info', 'dest_host', 'domain', 'event_code', 'event_id', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'login_id', 'object', 'process_dir', 'process_name', 'process_path', 'result', 'share_name', 'src_host', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['({dest_host}({host}[\w\-.]+))\s+ADAuditPlus'] |
| edit_regex_field | object |  | ['\WOBJECT_NAME\s*=\s*(?:[\\?]*)(null|({file_path}({object}[^\]]+?)))\s*\]'] |
| added_regex_field | dest_host |  | ['({dest_host}({host}[\w\-.]+))\s+ADAuditPlus'] |
| added_regex_field | file_path |  | ['\WOBJECT_NAME\s*=\s*(?:[\\?]*)(null|({file_path}({object}[^\]]+?)))\s*\]'] |
| removed_attribute | DupFields |  | N/A |