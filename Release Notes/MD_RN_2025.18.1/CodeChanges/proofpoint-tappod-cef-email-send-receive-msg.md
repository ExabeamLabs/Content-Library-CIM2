# Code Changes for proofpoint-tappod-cef-email-send-receive-msg (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_id', 'alert_name', 'bytes', 'direction', 'email_subject', 'host', 'num_recipients', 'time'] |
| removed_regex_field | routes |  | [] |
| added_regex_field | direction |  | ['\sroutes=({direction}[^=]+?)\s+(\w+=|$)'] |