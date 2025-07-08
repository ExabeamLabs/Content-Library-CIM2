# Code Changes for microsoft-azureadip-cef-alert-trigger-success-logininfected (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'app', 'dest_ip', 'dest_port', 'email_address', 'email_domain', 'email_recipients', 'file_ext', 'file_name', 'hash_md5', 'malware_file_name', 'result', 'time'] | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'app', 'dest_ip', 'dest_port', 'email_address', 'email_domain', 'email_recipients', 'file_ext', 'file_name', 'hash_sha256', 'malware_file_name', 'result', 'time'] |
| removed_regex_field | hash_md5 | ['SHA256\\?"*:\s*\\?"*({hash_md5}[^"\\]+)\\?"+'] | [] |
| added_regex_field | hash_sha256 | [] | ['SHA256\\?"*:\s*\\?"*({hash_sha256}[^"\\]+)\\?"+'] |