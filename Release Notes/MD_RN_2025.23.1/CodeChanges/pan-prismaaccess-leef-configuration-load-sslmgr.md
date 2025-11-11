# Code Changes for pan-prismaaccess-leef-configuration-load-sslmgr (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'bytes', 'bytes_in', 'bytes_out', 'category', 'dest_interface', 'dest_ip', 'dest_network_zone', 'dest_port', 'dest_translated_ip', 'direction', 'domain', 'email_address', 'event_category', 'event_name', 'failure_reason', 'host', 'network_app', 'protocol', 'result', 'rule', 'session_id', 'severity', 'src_interface', 'src_ip', 'src_network_zone', 'src_port', 'src_translated_ip', 'subtype', 'time', 'uri_path', 'uri_query', 'url', 'user', 'web_domain'] |
| edit_regex_field | result |  | ['EventStatus=({action}({result}[^\s=]+))', '\sAction=({action}({result}[^=]+?))\s\w+='] |
| added_regex_field | action |  | ['EventStatus=({action}({result}[^\s=]+))', '\sAction=({action}({result}[^=]+?))\s\w+='] |
| removed_attribute | DupFields |  | N/A |