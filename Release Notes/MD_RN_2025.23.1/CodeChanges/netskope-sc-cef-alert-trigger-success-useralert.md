# Code Changes for netskope-sc-cef-alert-trigger-success-useralert (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'app', 'browser', 'bytes', 'domain', 'email_address', 'file_name', 'file_type', 'object', 'operation', 'os', 'rule', 'rule_count', 'src_country', 'src_host', 'src_ip', 'src_location', 'time', 'url', 'user'] |
| edit_regex_field | object |  | ['"object":\s*"(((?i)(Unknown( Unknown)?)|null)|({file_name}({object}[^"]+?)))\s*"'] |
| added_regex_field | file_name |  | ['"object":\s*"(((?i)(Unknown( Unknown)?)|null)|({file_name}({object}[^"]+?)))\s*"'] |
| removed_attribute | DupFields |  | N/A |