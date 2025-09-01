# Code Changes for amazon-awsguardduty-json-alert-trigger-success-guardduty-portprobeunprotectedport (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | role |  | ['exa_regex=AssumedRole\/({role}[^\s]+)', 'exa_regex=AssumedRole\s+:\s+({role}[^\s]+)'] |