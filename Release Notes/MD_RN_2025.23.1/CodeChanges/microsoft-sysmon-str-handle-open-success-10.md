# Code Changes for microsoft-sysmon-str-handle-open-success-10 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | event_code |  | ['\Weventrecordid="+({event_code}({event_id}\d+))"', 'eventid="+({event_code}\d+)'] |
| edit_regex_field | event_id |  | ['\Weventrecordid="+({event_code}({event_id}\d+))"'] |
| removed_attribute | DupFields |  | N/A |