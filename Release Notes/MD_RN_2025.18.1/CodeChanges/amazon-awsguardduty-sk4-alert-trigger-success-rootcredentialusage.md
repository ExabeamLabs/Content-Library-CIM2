# Code Changes for amazon-awsguardduty-sk4-alert-trigger-success-rootcredentialusage (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | role |  | ['exa_regex=AssumedRole\/({role}[^\s]+)', 'exa_regex=AssumedRole\s+:\s+({role}[^\s]+)'] |