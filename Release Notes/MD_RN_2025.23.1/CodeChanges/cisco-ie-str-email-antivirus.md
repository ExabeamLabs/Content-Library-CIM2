# Code Changes for cisco-ie-str-email-antivirus (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'malware_score', 'message_id'] |
| added_regex_field | message_id |  | ['MID ({message_id}\d+)'] |
| removed_attribute | DupFields |  | N/A |