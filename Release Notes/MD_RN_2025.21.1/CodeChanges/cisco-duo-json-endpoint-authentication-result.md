# Code Changes for cisco-duo-json-endpoint-authentication-result (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'auth_method', 'device_name', 'domain', 'failure_reason', 'host', 'mfa_device', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | device_name |  | ['"+device"+:\s(null|"+({mfa_device}({device_name}[^"]+)))'] |
| added_regex_field | mfa_device |  | ['"+device"+:\s(null|"+({mfa_device}({device_name}[^"]+)))'] |
| removed_attribute | DupFields |  | N/A |