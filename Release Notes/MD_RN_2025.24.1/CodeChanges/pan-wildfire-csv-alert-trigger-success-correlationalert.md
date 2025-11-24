# Code Changes for pan-wildfire-csv-alert-trigger-success-correlationalert (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_subject', 'alert_type', 'app', 'category', 'domain', 'host', 'malware_url', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | additional_info |  | [',CORRELATION,([^,]*,){17}\\?"*\s*({additional_info}({alert_subject}({alert_name}[^\.,]+))[^\.]*)\.'] |
| edit_regex_field | alert_name |  | [',CORRELATION,([^,]*,){15}({app}({alert_subject}({alert_name}[^,]+)))', ',CORRELATION,([^,]*,){17}\\?"*\s*({additional_info}({alert_subject}({alert_name}[^\.,]+))[^\.]*)\.'] |
| edit_regex_field | alert_type |  | [',CORRELATION,([^,]*,){6}({category}({alert_type}[^,]+))'] |
| added_regex_field | alert_subject |  | [',CORRELATION,([^,]*,){15}({app}({alert_subject}({alert_name}[^,]+)))', ',CORRELATION,([^,]*,){17}\\?"*\s*({additional_info}({alert_subject}({alert_name}[^\.,]+))[^\.]*)\.'] |
| added_regex_field | app |  | [',CORRELATION,([^,]*,){15}({app}({alert_subject}({alert_name}[^,]+)))'] |
| added_regex_field | category |  | [',CORRELATION,([^,]*,){6}({category}({alert_type}[^,]+))'] |
| removed_attribute | DupFields |  | N/A |