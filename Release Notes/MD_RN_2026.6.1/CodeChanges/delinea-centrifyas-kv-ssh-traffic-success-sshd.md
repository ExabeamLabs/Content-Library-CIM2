# Code Changes for delinea-centrifyas-kv-ssh-traffic-success-sshd (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth', 'dest_host', 'domain', 'event_name', 'host', 'process_id', 'process_path', 'result', 'src_host', 'src_ip', 'time', 'user'] |
| edit_regex_field | dest_host |  | ['EntityName=({domain}[^\\]+)\\+({dest_host}[\w\-\.]+)'] |
| added_regex_field | domain |  | ['EntityName=({domain}[^\\]+)\\+({dest_host}[\w\-\.]+)'] |