# Code Changes for citrix-cgateway-str-vpn-authentication-success-succeededpolicy (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_method', 'auth_type', 'domain', 'email_address', 'event_code', 'event_name', 'host', 'src_host', 'time', 'user'] |
| edit_regex_field | host |  | ['\s*(GMT)?\s*({src_host}({host}[^:\s]+))\s*\S+\s*:\s\w+\sAAA Message'] |
| added_regex_field | auth_type |  | ['\s*=\s*({auth_type}[^\s"]+)"?'] |
| added_regex_field | src_host |  | ['\s*(GMT)?\s*({src_host}({host}[^:\s]+))\s*\S+\s*:\s\w+\sAAA Message'] |
| removed_attribute | DupFields |  | N/A |