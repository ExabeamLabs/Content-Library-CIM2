# Code Changes for vmware-carbonblack-sk4-alert-trigger-success-cbanalytics (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'category', 'dest_process_path', 'domain', 'email_address', 'hash_sha256', 'host', 'policy_name', 'primary_key', 'process_dir', 'process_name', 'result', 'src_ip', 'src_port', 'status_msg', 'threat_id', 'time', 'user'] |
| removed_regex_field | state |  | [] |
| added_regex_field | status_msg |  | ['"+state"+:\s*"+({status_msg}[^"]+?)"+'] |