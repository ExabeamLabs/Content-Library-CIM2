# Code Changes for cisco-ie-str-email-subject (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'email_subject', 'message_id'] |
| edit_regex_field | alert_id |  | ['MID ({alert_id}\d+) Subject (\'|")?({email_subject}.+?)\s*(\'|"|$)', '\sMID\s+({message_id}({alert_id}\d+))'] |
| added_regex_field | message_id |  | ['\sMID\s+({message_id}({alert_id}\d+))'] |
| removed_attribute | DupFields |  | N/A |