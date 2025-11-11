# Code Changes for cisco-ie-cef-email-graymail (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'graymail_score', 'host', 'message_id', 'time'] |
| added_regex_field | message_id |  | ['MID ({message_id}\d+)'] |
| removed_attribute | DupFields |  | N/A |