# Code Changes for cisco-ie-cef-email-antivirus (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'host', 'malware_score', 'message_id', 'src_ip', 'time'] |
| added_regex_field | message_id |  | ['MID ({message_id}\d+)'] |
| removed_attribute | DupFields |  | N/A |