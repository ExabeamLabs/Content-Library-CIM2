# Code Changes for amazon-awscloudtrail-sk4-app-activity-aws (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'aws_account', 'aws_email_address', 'bucket_name', 'domain', 'email_address', 'email_domain', 'event_name', 'object', 'operation', 'process_name', 'region', 'role', 'time', 'user'] |
| edit_regex_field | process_name |  | ['\Wdproc=({process_name}[^\[\]]+?)\s+(\w+=|$)'] |
| added_regex_field | region |  | ['"awsRegion"\s*:\s*"({region}[^"]+)"', '\WResources":.+?"Region":"({region}[^"]+)"', 'exa_regex=\WawsRegion":"({region}[^"]+)"'] |