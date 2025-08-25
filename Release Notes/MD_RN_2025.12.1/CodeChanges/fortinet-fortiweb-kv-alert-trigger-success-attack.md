# Code Changes for fortinet-fortiweb-kv-alert-trigger-success-attack (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| COULD_NOT_COMPARE | TimeFormat | epoch_sec | ['epoch_sec', "yyyy-MM-dd 'time='HH:mm:ss"] |
| changed_parsed_fields | N/A | ['action', 'additional_info', 'alert_name', 'alert_reason', 'alert_severity', 'alert_type', 'dest_ip', 'dest_port', 'domain', 'email_address', 'host', 'method', 'policy_name', 'protocol', 'referrer', 'src_ip', 'src_port', 'time', 'uri_path', 'uri_query', 'user', 'user_agent', 'web_domain'] | ['action', 'additional_info', 'alert_name', 'alert_reason', 'alert_severity', 'alert_type', 'category', 'dest_ip', 'dest_port', 'domain', 'email_address', 'host', 'method', 'policy_name', 'protocol', 'referrer', 'session_id', 'src_country', 'src_ip', 'src_port', 'threat_handled', 'time', 'uri_path', 'uri_query', 'user', 'user_agent', 'version', 'vm_pool_name', 'web_domain'] |
| edit_regex_field | alert_reason | ['signature_subclass="({alert_reason}[^"]+)"'] | ['signature_subclass="(N\/A|({alert_reason}[^"]+))"'] |
| edit_regex_field | time | ['timestamp=({time}\d{10})'] | ['date="*({time}\d\d\d\d-\d\d-\d\d time=\d\d:\d\d:\d\d)', 'timestamp=({time}\d{10})'] |
| added_regex_field | category | [] | ['\Wtype=({category}[^"]+)\s'] |
| added_regex_field | session_id | [] | ['http_session_id="(none|({session_id}[^"]+))'] |
| added_regex_field | src_country | [] | ['\ssrccountry=\\?"?({src_country}[^=]+?)\\?"?\s+(\w+=|$)'] |
| added_regex_field | threat_handled | [] | ['false_positive_mitigation="(none|({threat_handled}[^"]+))"'] |
| added_regex_field | version | [] | ['http_version="({version}[^"]+)'] |
| added_regex_field | vm_pool_name | [] | ['server_pool_name="(none|({vm_pool_name}[^"]+))"'] |