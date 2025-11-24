# Code Changes for zyxel-usgflex-kv-network-session-fail-accessblock (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['category', 'dest_ip', 'dest_port', 'devid', 'direction', 'email_address', 'email_domain', 'event_name', 'failure_reason', 'host', 'operation', 'protocol', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | failure_reason |  | ['\snote="({failure_reason}[^"]+)'] |
| removed_attribute | DupFields |  | N/A |