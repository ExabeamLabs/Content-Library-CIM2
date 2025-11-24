# Code Changes for mcafee-sncasb-kv-alert-trigger-success-timeupdated (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_name', 'alert_severity', 'alert_type', 'bytes', 'dest_host', 'host', 'time', 'user'] |
| edit_regex_field | alert_name |  | [',userAction=({alert_type}({alert_name}[^,]+))'] |
| added_regex_field | alert_type |  | [',userAction=({alert_type}({alert_name}[^,]+))'] |
| removed_attribute | DupFields |  | N/A |