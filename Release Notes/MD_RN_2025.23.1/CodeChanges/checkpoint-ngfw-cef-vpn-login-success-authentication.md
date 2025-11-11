# Code Changes for checkpoint-ngfw-cef-vpn-login-success-authentication (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_severity', 'bytes', 'bytes_in', 'bytes_out', 'company', 'department', 'dest_ip', 'dest_port', 'dest_translated_ip', 'direction', 'domain', 'email_address', 'first_name', 'full_name', 'host', 'last_name', 'origin_ip', 'os', 'product_name', 'protocol', 'result', 'rule', 'src_host', 'src_interface', 'src_ip', 'src_port', 'src_translated_ip', 'time', 'tunnel_protocol', 'user', 'user_ou'] |
| edit_regex_field | result |  | ['\Wact=(|({result}.+?))(\s+\w+=|\s*$)', 'categoryOutcome=(\/)?({result}.+?)\s\w+='] |
| added_regex_field | bytes |  | ['\Wout=({bytes}\d+)', '\Wserver_outbound_bytes=({bytes}\d+)'] |