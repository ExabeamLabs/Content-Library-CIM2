# Code Changes for cyberark-pam-cef-app-login-success-logon (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A | ['app', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'email_address', 'event_code', 'event_id', 'host', 'operation', 'severity', 'src_host', 'src_ip', 'src_port', 'time', 'user'] | ['app', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'email_address', 'event_code', 'host', 'operation', 'severity', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | event_code | ['Cyber-Ark|Vault\|[^\|]+\|({event_code}\d+)'] | ['Cyber-Ark\|Vault\|[^\|]+\|({event_code}\d+)'] |
| removed_regex_field | event_id | ['Cyber-Ark|Vault\|[^\|]+\|({event_id}\d+)'] | [] |