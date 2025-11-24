# Code Changes for forescout-couteract-cef-alert-trigger-success-rule (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'alert_type', 'dest_ip', 'dest_port', 'host', 'host_ip'] |
| edit_regex_field | alert_name |  | ['Rule:\s*(|({alert_type}({alert_name}Policy\s+\"*[^\"]+?\s*\"*)))\s*,'] |
| added_regex_field | alert_type |  | ['Rule:\s*(|({alert_type}({alert_name}Policy\s+\"*[^\"]+?\s*\"*)))\s*,'] |
| removed_attribute | DupFields |  | N/A |