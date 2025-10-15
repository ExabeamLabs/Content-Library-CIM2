# Code Changes for ibm-guardium-str-alert-trigger-success-mssql (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'additional_info', 'alert_name', 'alert_severity', 'alert_type', 'db_name', 'db_user', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'host', 'process_dir', 'process_name', 'process_path', 'server_group', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | db_user |  | ['DB User:\s*(({domain}\w+)\\)?({account}({db_user}[\w\d]+))(\s+\(.+?\))?([#\d\\n]+)?([\w\s]+:)'] |
| edit_regex_field | domain |  | ['DB User:\s*(({domain}\w+)\\)?({account}({db_user}[\w\d]+))(\s+\(.+?\))?([#\d\\n]+)?([\w\s]+:)'] |
| added_regex_field | account |  | ['DB User:\s*(({domain}\w+)\\)?({account}({db_user}[\w\d]+))(\s+\(.+?\))?([#\d\\n]+)?([\w\s]+:)'] |
| removed_attribute | DupFields |  | N/A |