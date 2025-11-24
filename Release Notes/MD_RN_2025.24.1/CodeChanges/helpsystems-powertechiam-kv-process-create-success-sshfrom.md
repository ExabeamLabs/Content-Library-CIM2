# Code Changes for helpsystems-powertechiam-kv-process-create-success-sshfrom (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'dest_host', 'event_code', 'host', 'process_command_line', 'src_ip', 'time', 'user'] |
| edit_regex_field | host |  | ['\d\dZ\s+({dest_host}({host}[\w\-.]+))\s+sshd - ssh_runcmd'] |
| added_regex_field | dest_host |  | ['\d\dZ\s+({dest_host}({host}[\w\-.]+))\s+sshd - ssh_runcmd'] |
| removed_attribute | DupFields |  | N/A |