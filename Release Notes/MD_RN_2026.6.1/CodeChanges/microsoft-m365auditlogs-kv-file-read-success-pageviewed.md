# Code Changes for microsoft-m365auditlogs-kv-file-read-success-pageviewed (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'channel', 'domain', 'email_address', 'event_name', 'file_ext', 'file_name', 'file_path', 'file_type', 'object', 'operation', 'result', 'src_ip', 'src_port', 'time', 'user', 'user_agent'] |
| added_regex_field | file_path |  | ['OBJECT=(Unknown \(Unknown\)|({file_path}[^=]+?))\s+\w+='] |