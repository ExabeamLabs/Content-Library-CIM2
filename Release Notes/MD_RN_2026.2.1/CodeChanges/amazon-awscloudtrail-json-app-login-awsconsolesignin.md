# Code Changes for amazon-awscloudtrail-json-app-login-awsconsolesignin (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'assumedRoleId', 'aws_account', 'aws_email_address', 'aws_user', 'domain', 'email_address', 'email_domain', 'failure_reason', 'host', 'key_id', 'mfa', 'operation', 'region', 'result', 'role', 'session_name', 'src_ip', 'src_port', 'time', 'user', 'user_agent'] |
| added_regex_field | mfa |  | ['"MFAUsed":\s*"({mfa}[^"]+)"', '"mfaAuthenticated":\s*"({mfa}[^"]+)"'] |