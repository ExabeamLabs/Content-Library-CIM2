# Code Changes for crowdstrike-falcon-sk4-alert-trigger-lsasshandlefromunsignedmodule (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'aid', 'alert_name', 'alert_subject', 'cid', 'event_code', 'file_dir', 'file_ext', 'file_name', 'file_path', 'new_hash', 'old_hash', 'os', 'process_guid', 'process_name', 'process_path', 'src_file_dir', 'src_file_name', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | alert_name |  | ['"name":\s*"({alert_subject}({alert_name}[^",]+))"'] |
| added_regex_field | alert_subject |  | ['"name":\s*"({alert_subject}({alert_name}[^",]+))"'] |
| removed_attribute | DupFields |  | N/A |