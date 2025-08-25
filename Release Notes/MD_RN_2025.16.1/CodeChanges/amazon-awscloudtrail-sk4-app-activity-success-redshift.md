# Code Changes for amazon-awscloudtrail-sk4-app-activity-success-redshift (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'aws_account', 'aws_email_address', 'categories', 'domain', 'email_address', 'email_domain', 'event_name', 'region', 'role', 'severity', 'src_host', 'src_resource_type', 'time', 'user', 'user_id'] |
| added_regex_field | region |  | ['"awsRegion"\s*:\s*"({region}[^"]+)"', 'exa_regex=\WawsRegion":"({region}[^"]+)"'] |