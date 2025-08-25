# Code Changes for crowdstrike-falcon-json-alert-trigger-success-idpdetection (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'aid', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'category', 'dest_host', 'domain', 'email_address', 'email_domain', 'falcon_host_link', 'severity', 'src_domain', 'src_host', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| removed_regex_field | top_domain |  | [] |
| added_regex_field | src_domain |  | ['"SourceAccountDomain":"({src_domain}[^"]+)"', 'exa_regex="SourceAccountDomain":"({src_domain}[^"]+)"'] |