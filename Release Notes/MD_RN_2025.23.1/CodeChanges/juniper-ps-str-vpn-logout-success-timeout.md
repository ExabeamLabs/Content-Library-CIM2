# Code Changes for juniper-ps-str-vpn-logout-success-timeout (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'dest_ip', 'dest_port', 'domain', 'email_address', 'host', 'realm', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | host |  | ['PulseSecure:[\s\-]*({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)\s+\-\s+({dest_host}({host}[\w\-.]+))', '\d{4}-\d{2}-\d{2} \d\d:\d\d:\d\d\s+-\s+({dest_host}({host}[\w\.-]+))\s+-\s+\['] |
| edit_regex_field | time |  | ['({time}\d+-\d+-\d+ \d\d:\d\d:\d\d)', 'PulseSecure:[\s\-]*({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)\s+\-\s+({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_host |  | ['PulseSecure:[\s\-]*({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)\s+\-\s+({dest_host}({host}[\w\-.]+))', '\d{4}-\d{2}-\d{2} \d\d:\d\d:\d\d\s+-\s+({dest_host}({host}[\w\.-]+))\s+-\s+\['] |
| removed_attribute | DupFields |  | N/A |