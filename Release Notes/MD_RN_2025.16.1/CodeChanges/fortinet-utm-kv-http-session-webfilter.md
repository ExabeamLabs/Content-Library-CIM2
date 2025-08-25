# Code Changes for fortinet-utm-kv-http-session-webfilter (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_severity', 'asset_id', 'bytes_in', 'bytes_out', 'category', 'category_id', 'dest_ip', 'dest_port', 'direction', 'domain', 'email_address', 'host', 'method', 'policy_id', 'protocol', 'referrer', 'result_reason', 'src_ip', 'src_port', 'time', 'tz', 'uri_path', 'uri_query', 'url', 'user', 'user_group_name', 'web_domain'] |
| removed_regex_field | http_response_code |  | [] |
| added_regex_field | category_id |  | ['cat=({category_id}\d+)'] |