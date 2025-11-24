# Code Changes for blackberry-protect-sk4-alert-trigger-success-terminate (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_id', 'alert_name', 'alert_source', 'alert_subject', 'alert_type', 'device_id', 'file_ext', 'file_hash', 'file_name', 'hash_sha256', 'hash_sha256_at', 'name_at', 'process_dir', 'process_id', 'process_name', 'process_path', 'time', 'user', 'user_group_name'] |
| edit_regex_field | alert_name |  | [' Category \[({alert_subject}({alert_name}[^\]]+))\]'] |
| edit_regex_field | file_ext |  | ['\sfname=([^=]*\\)?({name_at}({file_name}[^\.]+\.({file_ext}[^\\:\s.]+)?))\s+\w+='] |
| edit_regex_field | file_hash |  | ['"file_hash_id":"({hash_sha256_at}({file_hash}[^"]+))"'] |
| edit_regex_field | file_name |  | ['\sfname=([^=]*\\)?({name_at}({file_name}[^\.]+\.({file_ext}[^\\:\s.]+)?))\s+\w+='] |
| added_regex_field | alert_subject |  | [' Category \[({alert_subject}({alert_name}[^\]]+))\]'] |
| added_regex_field | hash_sha256_at |  | ['"file_hash_id":"({hash_sha256_at}({file_hash}[^"]+))"'] |
| added_regex_field | name_at |  | ['\sfname=([^=]*\\)?({name_at}({file_name}[^\.]+\.({file_ext}[^\\:\s.]+)?))\s+\w+='] |
| removed_attribute | DupFields |  | N/A |