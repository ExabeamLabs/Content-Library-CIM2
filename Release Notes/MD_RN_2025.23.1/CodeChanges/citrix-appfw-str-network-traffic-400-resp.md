# Code Changes for citrix-appfw-str-network-traffic-400-resp (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_id', 'alert_name', 'event_code', 'event_name', 'failure_reason', 'host', 'interface_in', 'result', 'rule', 'src_ip', 'src_port', 'time', 'url'] |
| edit_regex_field | event_code |  | ['\s({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d)\s+(GMT|({host}\S+))\s+({interface_in}\S+)\s+:\s+(\S+\s+){2}({alert_name}({event_name}\S+))\s+({event_code}\S+)'] |
| edit_regex_field | event_name |  | ['\s({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d)\s+(GMT|({host}\S+))\s+({interface_in}\S+)\s+:\s+(\S+\s+){2}({alert_name}({event_name}\S+))\s+({event_code}\S+)'] |
| edit_regex_field | host |  | ['\s({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d)\s+(GMT|({host}\S+))\s+({interface_in}\S+)\s+:\s+(\S+\s+){2}({alert_name}({event_name}\S+))\s+({event_code}\S+)'] |
| edit_regex_field | interface_in |  | ['\s({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d)\s+(GMT|({host}\S+))\s+({interface_in}\S+)\s+:\s+(\S+\s+){2}({alert_name}({event_name}\S+))\s+({event_code}\S+)'] |
| edit_regex_field | time |  | ['\s({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d)\s+(GMT|({host}\S+))\s+({interface_in}\S+)\s+:\s+(\S+\s+){2}({alert_name}({event_name}\S+))\s+({event_code}\S+)'] |
| added_regex_field | alert_name |  | ['\s({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d)\s+(GMT|({host}\S+))\s+({interface_in}\S+)\s+:\s+(\S+\s+){2}({alert_name}({event_name}\S+))\s+({event_code}\S+)'] |
| removed_attribute | DupFields |  | N/A |