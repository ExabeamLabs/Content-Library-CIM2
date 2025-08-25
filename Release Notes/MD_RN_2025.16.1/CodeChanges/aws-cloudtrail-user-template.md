# Code Changes for aws-cloudtrail-user-template (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['aws_account', 'aws_email_address', 'domain', 'email_address', 'email_domain', 'region', 'role', 'user'] |
| added_regex_field | region |  | ['"awsRegion"\s*:\s*"({region}[^"]+)"', 'exa_regex=\WawsRegion":"({region}[^"]+)"'] |