# Code Changes for s-cisco-amp-alert (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_name', 'alert_severity', 'alert_type', 'category', 'connector_guid', 'dest_ip', 'dest_port', 'domain', 'email_address', 'email_domain', 'event_name', 'file_name', 'file_path', 'hash_md5', 'hash_sha1', 'hash_sha256', 'malware_file_name', 'product_name', 'result', 'src_host', 'src_ip', 'src_mac', 'src_port', 'time', 'user'] |
| edit_regex_field | alert_name |  | ['"detection":\s*"(|({alert_name}[^"]+?))"', 'dpriv=({alert_name}[^=]+?)\s\w+=', 'event_type":\s*"({alert_name}[^"]+)'] |
| added_regex_field | category |  | ['event_type":\s*"({category}[^"]+)', 'exa_regex=event_type":\s*"({category}[^"]+)'] |
| added_regex_field | malware_file_name |  | ['file_path":\s*"(\\+\?\\+)?({malware_file_name}[^"]+)'] |
| removed_attribute | DupFields |  | N/A |