# Code Changes for cisco-secureendpoint-sk4-alert-trigger-success-threatdetection (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_name', 'alert_severity', 'alert_type', 'connector_guid', 'dest_ip', 'dest_port', 'domain', 'email_address', 'file_name', 'file_path', 'hash_md5', 'hash_sha1', 'hash_sha256', 'process_dir', 'process_name', 'product_name', 'result', 'src_host', 'src_ip', 'src_mac', 'src_port', 'time', 'user'] |
| edit_regex_field | process_name |  | ['"file":\{"name":\["({process_name}[^",]+)[^\s]+,"path":\["({process_dir}[^"]+)'] |
| removed_regex_field | process_path |  | [] |
| added_regex_field | process_dir |  | ['"file":\{"name":\["({process_name}[^",]+)[^\s]+,"path":\["({process_dir}[^"]+)'] |