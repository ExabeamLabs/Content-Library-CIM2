# Code Changes for amazon-awsguardduty-cef-alert-trigger-success-catsecurity (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | role |  | ['exa_regex=AssumedRole\/({role}[^\s]+)', 'exa_regex=AssumedRole\s+:\s+({role}[^\s]+)'] |