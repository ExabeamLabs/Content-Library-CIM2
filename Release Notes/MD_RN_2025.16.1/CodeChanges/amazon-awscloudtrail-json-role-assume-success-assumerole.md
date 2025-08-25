# Code Changes for amazon-awscloudtrail-json-role-assume-success-assumerole (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | region |  | ['"awsRegion"\s*:\s*"({region}[^"]+)"', '"awsRegion"\s*:\s*"({region}[^"]+)"', 'exa_regex=\WawsRegion":"({region}[^"]+)"'] |