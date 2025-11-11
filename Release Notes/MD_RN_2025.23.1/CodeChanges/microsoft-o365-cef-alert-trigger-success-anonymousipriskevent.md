# Code Changes for microsoft-o365-cef-alert-trigger-success-anonymousipriskevent (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | alert_name |  | ['"riskEventType":\"({alert_name}[^\"]+?)\"', '({alert_name}({alert_type}anomalous-signin))'] |
| edit_regex_field | alert_type |  | ['({alert_name}({alert_type}anomalous-signin))'] |
| removed_attribute | DupFields |  | N/A |