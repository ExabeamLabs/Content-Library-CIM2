# Code Changes for amazon-awsguardduty-sk4-alert-trigger-success-guardduty-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'app', 'aws_account', 'aws_email_address', 'aws_user', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'email_address', 'email_domain', 'event_name', 'instance_id', 'instance_profile_arn', 'key_id', 'location_city', 'object', 'region', 'resource_type', 'result', 'role', 'src_ip', 'src_port', 'tags', 'time', 'user', 'user_type'] |
| added_regex_field | role |  | ['exa_regex=AssumedRole\/({role}[^\s]+)'] |