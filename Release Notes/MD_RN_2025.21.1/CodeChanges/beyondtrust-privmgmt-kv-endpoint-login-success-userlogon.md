# Code Changes for beyondtrust-privmgmt-kv-endpoint-login-success-userlogon (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['admin', 'dest_host', 'domain', 'host', 'operation_type', 'power_user', 'src_ip', 'src_port', 'user', 'user_info', 'user_sid'] |
| edit_regex_field | host |  | ['ComputerName=({dest_host}({host}[^\s]+))'] |
| added_regex_field | dest_host |  | ['ComputerName=({dest_host}({host}[^\s]+))'] |
| removed_attribute | DupFields |  | N/A |