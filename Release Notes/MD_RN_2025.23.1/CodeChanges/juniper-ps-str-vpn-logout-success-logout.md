# Code Changes for juniper-ps-str-vpn-logout-success-logout (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'dest_ip', 'dest_port', 'domain', 'email_address', 'host', 'realm', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | host |  | ['(Juniper|PulseSecure):\s*({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)\s+\-\s+({dest_host}({host}[\w\-.]+))'] |
| edit_regex_field | time |  | ['(Juniper|PulseSecure):\s*({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)\s+\-\s+({dest_host}({host}[\w\-.]+))', '({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d) \- .*?Logout from'] |
| added_regex_field | dest_host |  | ['(Juniper|PulseSecure):\s*({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)\s+\-\s+({dest_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |