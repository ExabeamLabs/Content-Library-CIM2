# Code Changes for amazon-awscloudtrail-json-bucket-policy-modify-putbucketpolicy (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | readonly |  | ['"readOnly"\s*:\s*"?({readonly}[^",\}]+)("|,|\}\s*$)'] |