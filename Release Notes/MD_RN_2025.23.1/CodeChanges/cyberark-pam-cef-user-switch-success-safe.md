# Code Changes for cyberark-pam-cef-user-switch-success-safe (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'action', 'additional_info', 'dest_host', 'dest_ip', 'dest_port', 'dest_user', 'device_type', 'domain', 'event_code', 'event_name', 'host', 'safe_value', 'severity', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | account |  | ['\sduser="?([^\\="]+\\+)?({account}[^="]+?)"?\s+\w+=', '\sfname=[^=]+?\-({account}[^\s-]+?)\s+\w+='] |
| removed_attribute | DupFields |  | N/A |