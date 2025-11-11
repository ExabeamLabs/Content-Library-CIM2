# Code Changes for citrix-netscalerwaf-str-network-traffic-ssl-handshake (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['event_name', 'host', 'operation', 'protocol', 'result', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | event_name |  | ['({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d\s*GMT)\s({host}[^\s]+).*?:\sdefault\s({protocol}[^\s]+)\s({operation}({event_name}[^\s]+))'] |
| edit_regex_field | host |  | ['({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d\s*GMT)\s({host}[^\s]+).*?:\sdefault\s({protocol}[^\s]+)\s({operation}({event_name}[^\s]+))'] |
| edit_regex_field | protocol |  | ['({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d\s*GMT)\s({host}[^\s]+).*?:\sdefault\s({protocol}[^\s]+)\s({operation}({event_name}[^\s]+))'] |
| edit_regex_field | time |  | ['({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d\s*GMT)\s({host}[^\s]+).*?:\sdefault\s({protocol}[^\s]+)\s({operation}({event_name}[^\s]+))'] |
| added_regex_field | operation |  | ['({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d\s*GMT)\s({host}[^\s]+).*?:\sdefault\s({protocol}[^\s]+)\s({operation}({event_name}[^\s]+))'] |
| removed_attribute | DupFields |  | N/A |