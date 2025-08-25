# Code Changes for symantec-dlp-leef-alert-email-modified (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'action', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'bytes', 'bytes_unit', 'dest_ip', 'domain', 'email_address', 'email_domain', 'email_recipients', 'email_subject', 'file_dir', 'file_name', 'host', 'protocol', 'src_ip', 'target', 'time', 'url', 'user', 'web_domain'] |
| removed_regex_field | file_path |  | [] |
| added_regex_field | file_dir |  | ['\|parentPath=(N\/A|({file_dir}[^\|]+))'] |