# Code Changes for amazon-awsguardduty-sk4-alert-trigger-success-anomalousbehavior (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | instance_profile_arn |  | ['"+iamInstanceProfile.+?arn\\?":\s*\\?"({instance_profile_arn}[^"]+?)\\?"', 'exa_regex="+iamInstanceProfile.+?arn\\?":\s*\\?"({instance_profile_arn}[^"]+?)\\?"'] |