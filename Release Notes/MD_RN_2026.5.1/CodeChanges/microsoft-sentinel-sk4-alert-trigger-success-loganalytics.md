# Code Changes for microsoft-sentinel-sk4-alert-trigger-success-loganalytics (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'channel', 'dns_domain', 'domain', 'domain_join', 'end_time', 'host', 'is_incident', 'login_id', 'malware_url', 'nt_domain', 'process_command_line', 'process_dir', 'process_name', 'process_path', 'processing_end_time', 'remediation_steps', 'src_host', 'start_time', 'tenant_id', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"Channel"+:"+({channel}[^"]+)"'] |
| added_regex_field | tenant_id |  | ['"(?i:tenantid)":"({tenant_id}[^"]+)'] |