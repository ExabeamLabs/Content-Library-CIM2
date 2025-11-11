# Code Changes for cisco-ie-str-email-aborted (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'failure_reason', 'message_id', 'result', 'time'] |
| added_regex_field | message_id |  | ['\sMID\s+({message_id}\d+)'] |
| removed_attribute | DupFields |  | N/A |