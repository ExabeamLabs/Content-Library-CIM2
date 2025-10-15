# Code Changes for rsa-securid-kv-endpoint-login-fail-tokenauth (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_ip', 'dest_port', 'failure_reason', 'host', 'policy_name', 'result', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | additional_info |  | ['DESCRIPTION="({failure_reason}({additional_info}[^".]+))'] |
| added_regex_field | failure_reason |  | ['DESCRIPTION="({failure_reason}({additional_info}[^".]+))'] |
| removed_attribute | DupFields |  | N/A |