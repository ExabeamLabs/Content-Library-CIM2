# Code Changes for cisco-secureendpoint-sk4-alert (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_name', 'alert_severity', 'alert_type', 'category', 'connector_guid', 'dest_ip', 'dest_port', 'domain', 'email_address', 'event_name', 'file_name', 'file_path', 'hash_md5', 'hash_sha1', 'hash_sha256', 'malware_url', 'product_name', 'result', 'src_host', 'src_ip', 'src_mac', 'src_port', 'time', 'user'] |
| added_regex_field | category |  | ['event_type":\s*"({category}[^"]+)'] |
| added_regex_field | malware_url |  | ['file_path":\s*"(\\+\?\\+)?({malware_url}[^"]+)'] |
| removed_attribute | DupFields |  | N/A |