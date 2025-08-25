# Code Changes for amazon-awscloudwatch-sk4-app-activity-aws (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'alert_severity', 'app', 'aws_account', 'cluster_name', 'computer_name', 'domain', 'error_code', 'event_category', 'event_name', 'group_name', 'host', 'process_name', 'region', 'resource_id', 'result_code', 'src_ip', 'src_port', 'table', 'tenant_id', 'time', 'user', 'user_agent'] |
| added_regex_field | region |  | ['\WRegion\\*":\\*"({region}[^\\"]+?)\\*"', '\WResources":.+?"Region":"({region}[^"]+)"'] |