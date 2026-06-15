# Code Changes for f5-bigip-str-vpn-login-success-loggedonfrom (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['host', 'object', 'process_id', 'process_name', 'session_id', 'src_ip', 'time', 'user'] |
| removed_regex_field | dest_host |  | [] |
| added_regex_field | object |  | ['Node\s+=\s+({object}.+?)$'] |