# Code Changes for cisco-secureendpoint-sk4-alert-trigger-success-faultcleared (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_name', 'alert_severity', 'alert_type', 'category', 'connector_guid', 'dest_ip', 'dest_port', 'domain', 'email_address', 'event_name', 'hash_md5', 'hash_sha1', 'hash_sha256', 'process_path', 'product_name', 'result', 'src_file_name', 'src_file_path', 'src_host', 'src_ip', 'src_mac', 'src_port', 'time', 'user'] |
| added_regex_field | category |  | ['event_type":\s*"({category}[^"]+)'] |
| removed_attribute | DupFields |  | N/A |