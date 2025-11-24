# Code Changes for unix-ad-kv-process-create-success-audispd (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'host', 'host_ip', 'process_command_line', 'process_dir', 'process_id', 'process_name', 'result', 'src_host', 'time', 'user_id'] |
| edit_regex_field | host |  | ['\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?', '\s({src_host}({host}[\w\-.]+))\s+audisp', 'node=({src_host}({host}[^\s\.]+))'] |
| added_regex_field | src_host |  | ['\s({src_host}({host}[\w\-.]+))\s+audisp', 'node=({src_host}({host}[^\s\.]+))'] |
| removed_attribute | DupFields |  | N/A |