# Code Changes for cisco-ie-cef-email-spam (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'host', 'message_id', 'spam_score', 'src_ip', 'time'] |
| added_regex_field | message_id |  | ['MID ({message_id}\d+)'] |
| removed_attribute | DupFields |  | N/A |