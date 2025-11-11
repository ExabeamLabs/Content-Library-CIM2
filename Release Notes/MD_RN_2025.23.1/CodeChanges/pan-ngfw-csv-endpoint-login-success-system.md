# Code Changes for pan-ngfw-csv-endpoint-login-success-system (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'host', 'src_host', 'src_ip', 'time', 'user'] |
| added_regex_field | dest_host |  | [',SYSTEM,([^,]*,){18}({dest_host}[^\s,]+)'] |
| removed_attribute | DupFields |  | N/A |