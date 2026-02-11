# Code Changes for amazon-awscloudtrail-json-role-assume-success-assumerole (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'assumedRoleId', 'assumed_role_arn', 'aws_account', 'aws_email_address', 'domain', 'email_address', 'email_domain', 'event_category', 'event_id', 'failure_code', 'failure_reason', 'key_id', 'mfa', 'object', 'operation', 'principal_id', 'readonly', 'region', 'result', 'role', 'role_arn', 'role_id', 'service_name', 'session_arn', 'session_expiration', 'session_name', 'src_host', 'src_ip', 'src_port', 'time', 'user', 'user_agent', 'user_arn', 'user_type', 'vpc'] |
| removed_regex_field | event_code |  | [] |
| added_regex_field | event_id |  | ['"eventID\\?"+:\\?"+({event_id}[^"\\]+)\\?"'] |