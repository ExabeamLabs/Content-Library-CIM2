# Code Changes for zyxel-network-events (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['bytes_in', 'bytes_out', 'category', 'dest_ip', 'dest_port', 'devid', 'email_address', 'email_domain', 'event_name', 'host', 'operation', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | bytes_in |  | ['rcvd=({bytes_in}\d+)'] |
| added_regex_field | bytes_out |  | ['sent=({bytes_out}\d+)'] |