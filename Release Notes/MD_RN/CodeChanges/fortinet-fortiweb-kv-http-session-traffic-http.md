# Code Changes for fortinet-fortiweb-kv-http-session-traffic-http (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A | ['additional_info', 'bytes_in', 'bytes_out', 'dest_ip', 'dest_port', 'domain', 'email_address', 'host', 'http_response_code', 'method', 'protocol', 'referrer', 'src_ip', 'src_port', 'time', 'uri_path', 'uri_query', 'user', 'user_agent'] | ['additional_info', 'bytes_in', 'bytes_out', 'category', 'dest_ip', 'dest_port', 'domain', 'email_address', 'host', 'http_response_code', 'method', 'protocol', 'referrer', 'session_id', 'src_country', 'src_ip', 'src_port', 'threat_handled', 'time', 'uri_path', 'uri_query', 'user', 'user_agent', 'version', 'vm_pool_name'] |
| added_regex_field | category | [] | ['\Wtype=({category}[^"]+)\s'] |
| added_regex_field | session_id | [] | ['http_session_id="(none|({session_id}[^"]+))'] |
| added_regex_field | src_country | [] | ['\ssrccountry=\\?"?({src_country}[^=]+?)\\?"?\s+(\w+=|$)'] |
| added_regex_field | threat_handled | [] | ['false_positive_mitigation="(none|({threat_handled}[^"]+))"'] |
| added_regex_field | version | [] | ['http_version="({version}[^"]+)'] |
| added_regex_field | vm_pool_name | [] | ['server_pool_name="(none|({vm_pool_name}[^"]+))"'] |