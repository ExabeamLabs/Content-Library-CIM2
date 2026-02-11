# Code Changes for checkpoint-avanan-json-email-send-avanansecurityevent (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | additional_info |  | ['("|\')description_text\\*("|\'):\\*("|\')({additional_info}[^\[]+?)\\*",'] |
| edit_regex_field | alert_id |  | ['("|\')entity_info\\*("|\'):\{[^\}]+?"entity_id\\*":\\*"({alert_id}[^"\\]+)'] |
| edit_regex_field | alert_name |  | ['("|\')(event|source)type\\*("|\'):\\*("|\')\s*({alert_name}[^\\"]+)'] |
| edit_regex_field | alert_severity |  | ['("|\')severity\\*("|\'):\s*({alert_severity}[^,]+?)\}?,'] |
| edit_regex_field | alert_type |  | ['("|\')entity_info\\*("|\'):\{[^\}]+?"entity_sub_type\\*":\\*"({alert_type}[^"\\]+)'] |
| edit_regex_field | category |  | ['("|\')category("|\'):\s*("|\')({category}[^"\']+)"'] |
| edit_regex_field | email_subject |  | ['("|\')(entity_)?payload\\*("|\'):\{[^\}]+?"subject\\*":\\*"\s*({email_subject}[^"\\]+?)\s*\\*"', '("|\')subject\\*("|\'):\s*("|\')({email_subject}[^\\"]+?)\s*\\*("|\')'] |
| edit_regex_field | full_name |  | ['("|\')saas_info\\*("|\'):\{[^\}]+?"full_name\\*":\\*"({full_name}[^\\"]+)\\*"'] |
| edit_regex_field | result |  | ['("|\')is_quarantined\\*("|\'):\s*({result}[^,]+)'] |
| edit_regex_field | src_ip |  | ['sender_client_ip\\*("|\'):\\*("|\')\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))'] |
| edit_regex_field | time |  | ['("|\')time("|\'):\s*("|\')({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)'] |