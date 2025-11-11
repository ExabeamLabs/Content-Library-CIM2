# Code Changes for microsoft-o365-cef-alert-trigger-success-alerttriggerd (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | alert_name |  | ['"(Name|an\\?)":\\?"({alert_subject}({alert_name}[^"]+?))(\\u200b)?\\?"'] |
| edit_regex_field | alert_subject |  | ['"(Name|an\\?)":\\?"({alert_subject}({alert_name}[^"]+?))(\\u200b)?\\?"', '"von\\*"*:\\*"*({alert_subject}[^",\\]+)'] |
| removed_attribute | DupFields |  | N/A |