# Code Changes for armis-a-cef-alert-trigger-success-systempolicyviolation-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions |  | ['"severity"', '"type":"', 'alertId"', 'policyTitle"'] |
| edit_regex_field | alert_type |  | ['"type":"({alert_type}[^"]+)'] |