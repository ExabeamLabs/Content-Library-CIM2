# Code Changes for delinea-centrifyas-cef-endpoint-login-fail-sshd (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_name', 'failure_reason', 'host', 'process_id', 'process_path', 'result', 'src_host', 'src_ip', 'time', 'user'] |
| edit_regex_field | dest_host |  | ['EntityName=({domain}[^\\]+)\\+({dest_host}[\w\-\.]+)'] |
| added_regex_field | domain |  | ['EntityName=({domain}[^\\]+)\\+({dest_host}[\w\-\.]+)'] |