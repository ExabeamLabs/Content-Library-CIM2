# Code Changes for f5-bigip-mix-vpn-login-success-01490500 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access_group', 'dest_host', 'domain', 'email_address', 'host', 'session_id', 'src_ip', 'src_port', 'user'] |
| edit_regex_field | host |  | ['"host":\{"name":"({dest_host}({host}[\w\-\.]+))', '\d\d:\d\d\s+({dest_host}({host}[^\s]+))\s([^\s]+\s)?[^\s]+\[\d+\]', 'exa_regex=\d\d:\d\d\s+({dest_host}({host}[^\s]+))\s([^\s]+\s)?[^\s]+\[\d+\]', 'exa_regex=hostname="({dest_host}({host}[\w\-\.]+))', 'hostname="({dest_host}({host}[\w\-\.]+))'] |
| added_regex_field | dest_host |  | ['"host":\{"name":"({dest_host}({host}[\w\-\.]+))', '\d\d:\d\d\s+({dest_host}({host}[^\s]+))\s([^\s]+\s)?[^\s]+\[\d+\]', 'exa_regex=\d\d:\d\d\s+({dest_host}({host}[^\s]+))\s([^\s]+\s)?[^\s]+\[\d+\]', 'exa_regex=hostname="({dest_host}({host}[\w\-\.]+))', 'hostname="({dest_host}({host}[\w\-\.]+))'] |
| removed_attribute | DupFields |  | N/A |