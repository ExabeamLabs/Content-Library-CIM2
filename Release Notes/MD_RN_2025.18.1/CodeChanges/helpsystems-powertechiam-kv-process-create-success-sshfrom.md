# Code Changes for helpsystems-powertechiam-kv-process-create-success-sshfrom (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'event_code', 'host', 'process_command_line', 'src_ip', 'time', 'user'] |
| removed_regex_field | path |  | [] |
| edit_regex_field | process_command_line |  | ['cmd="*({process_command_line}[^"]+?)"+\] ssh from'] |
| removed_regex_field | process_dir |  | [] |
| removed_regex_field | process_name |  | [] |