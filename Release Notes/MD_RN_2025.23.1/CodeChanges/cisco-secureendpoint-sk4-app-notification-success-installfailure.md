# Code Changes for cisco-secureendpoint-sk4-app-notification-success-installfailure (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_name', 'alert_severity', 'alert_type', 'categories', 'category', 'connector_guid', 'dest_ip', 'dest_port', 'domain', 'email_address', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'hash_md5', 'hash_sha1', 'hash_sha256', 'malware_url', 'process_path', 'product_name', 'src_host', 'src_ip', 'src_mac', 'src_port', 'time', 'user'] |
| edit_regex_field | alert_name |  | ['"detection":"(|({alert_name}[^"]+?))"', 'detection":\s*"({alert_name}[^"]+)', 'event_type":\s*"({alert_name}[^"]+)'] |
| edit_regex_field | file_dir |  | ['file_path":\s*"(\\+\?\\+)?({file_path}({file_dir}[^"]+[\\]+)?({file_name}[^"]+(\.({file_ext}[^"]+))))', 'file_path":\s*"(\\+\?\\+)?({malware_url}({file_dir}[^"]+[\\]+)?({file_name}[^"]+(\.({file_ext}[^"]+))))'] |
| edit_regex_field | file_ext |  | ['"file_name":\s*"({file_name}[^"]+(\.({file_ext}[^"]+)))', 'file_path":\s*"(\\+\?\\+)?({file_path}({file_dir}[^"]+[\\]+)?({file_name}[^"]+(\.({file_ext}[^"]+))))', 'file_path":\s*"(\\+\?\\+)?({malware_url}({file_dir}[^"]+[\\]+)?({file_name}[^"]+(\.({file_ext}[^"]+))))'] |
| edit_regex_field | file_name |  | ['"file_name":\s*"({file_name}[^"]+(\.({file_ext}[^"]+)))', ',\s*"disposition":.+?file_name":\s*"({file_name}[^"]+)', 'file_path":\s*"(\\+\?\\+)?({file_path}({file_dir}[^"]+[\\]+)?({file_name}[^"]+(\.({file_ext}[^"]+))))', 'file_path":\s*"(\\+\?\\+)?({malware_url}({file_dir}[^"]+[\\]+)?({file_name}[^"]+(\.({file_ext}[^"]+))))'] |
| added_regex_field | malware_url |  | ['file_path":\s*"(\\+\?\\+)?({malware_url}({file_dir}[^"]+[\\]+)?({file_name}[^"]+(\.({file_ext}[^"]+))))'] |
| removed_attribute | DupFields |  | N/A |