# Code Changes for cisco-ie-cef-email-subject (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'email_subject', 'host', 'message_id', 'src_ip', 'time'] |
| edit_regex_field | alert_id |  | ['MID ({message_id}({alert_id}\d+)) Subject ("|\')?({email_subject}[^\'=]+?)\s*(\'|"|$|\w+=)'] |
| edit_regex_field | email_subject |  | ['MID ({message_id}({alert_id}\d+)) Subject ("|\')?({email_subject}[^\'=]+?)\s*(\'|"|$|\w+=)'] |
| added_regex_field | message_id |  | ['MID ({message_id}({alert_id}\d+)) Subject ("|\')?({email_subject}[^\'=]+?)\s*(\'|"|$|\w+=)'] |
| removed_attribute | DupFields |  | N/A |