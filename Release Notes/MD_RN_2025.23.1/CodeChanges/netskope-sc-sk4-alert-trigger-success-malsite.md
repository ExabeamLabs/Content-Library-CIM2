# Code Changes for netskope-sc-sk4-alert-trigger-success-malsite (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_id', 'alert_name', 'alert_severity', 'alert_source', 'alert_type', 'dest_ip', 'dest_port', 'domain', 'email_address', 'malware_url', 'process_path', 'protocol', 'referrer', 'site_at', 'src_host', 'src_ip', 'src_port', 'threat_category', 'time', 'url', 'user', 'web_domain'] |
| added_regex_field | threat_category |  | ['"malsite_category":\["({threat_category}[^"]+)"[^\]]*?\]'] |
| removed_attribute | DupFields |  | N/A |