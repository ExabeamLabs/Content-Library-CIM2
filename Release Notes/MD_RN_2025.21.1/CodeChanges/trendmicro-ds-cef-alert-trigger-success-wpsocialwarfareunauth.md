# Code Changes for trendmicro-ds-cef-alert-trigger-success-wpsocialwarfareunauth (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'app', 'dest_host', 'dest_ip', 'dest_port', 'email_address', 'email_domain', 'hash_md5', 'host', 'malware_url', 'process_dir', 'process_name', 'process_path', 'result', 'src_host', 'src_ip', 'src_port', 'threat_type', 'time', 'user'] |
| edit_regex_field | result |  | ['\Wact=(Unknown|({action}({result}[^=]+?)))(?:\s+\w+=|\s*$|\s*")'] |
| added_regex_field | action |  | ['\Wact=(Unknown|({action}({result}[^=]+?)))(?:\s+\w+=|\s*$|\s*")'] |