# Code Changes for amazon-awscloudtrail-json-app-login-awsconsolesignin (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | region |  | ['"awsRegion":"({region}[^"]+)"', '"awsRegion"\s*:\s*"({region}[^"]+)"', 'exa_regex=\WawsRegion":"({region}[^"]+)"'] |