# Code Changes for microsoft-azureatp-json-alert-trigger-success-remoteexecutionsecurityalert (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_subject', 'alert_type', 'app', 'channel', 'dest_ip', 'dest_port', 'domain', 'email_address', 'email_domain', 'file_dir', 'file_ext', 'file_name', 'full_name', 'incident_status', 'location', 'result', 'src_host', 'src_ip', 'src_port', 'technique', 'tenant_id', 'time', 'user', 'user_upn'] |
| added_regex_field | channel |  | ['"Channel"+:"+({channel}[^"]+)"', '<Channel>({channel}[^<]+)<'] |
| added_regex_field | tenant_id |  | ['"azureTenantId":\s*"({tenant_id}[^"]+)"', '"tenantId"\s*:\s*"({tenant_id}[^"]+)"'] |