# Code Changes for citrix-netscalerwaf-str-network-traffic-default (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['bytes_in', 'bytes_out', 'dest_ip', 'dest_port', 'dest_translated_ip', 'dest_translated_port', 'email_address', 'event_name', 'failure_reason', 'host', 'operation', 'protocol', 'src_ip', 'src_port', 'src_translated_ip', 'src_translated_port', 'time', 'user'] |
| edit_regex_field | event_name |  | ['({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d\s*GMT)\s({host}[^\s]+).*?:\sdefault\s({protocol}[^\s]+)\s({operation}({event_name}[^\s]+))'] |
| edit_regex_field | host |  | ['({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d\s*GMT)\s({host}[^\s]+).*?:\sdefault\s({protocol}[^\s]+)\s({operation}({event_name}[^\s]+))'] |
| edit_regex_field | protocol |  | ['({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d\s*GMT)\s({host}[^\s]+).*?:\sdefault\s({protocol}[^\s]+)\s({operation}({event_name}[^\s]+))'] |
| edit_regex_field | time |  | ['({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d\s*GMT)\s({host}[^\s]+).*?:\sdefault\s({protocol}[^\s]+)\s({operation}({event_name}[^\s]+))'] |
| added_regex_field | operation |  | ['({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d\s*GMT)\s({host}[^\s]+).*?:\sdefault\s({protocol}[^\s]+)\s({operation}({event_name}[^\s]+))'] |
| removed_attribute | DupFields |  | N/A |