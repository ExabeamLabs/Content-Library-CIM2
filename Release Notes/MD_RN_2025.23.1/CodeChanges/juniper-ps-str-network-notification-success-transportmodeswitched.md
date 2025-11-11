# Code Changes for juniper-ps-str-network-notification-success-transportmodeswitched (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_host', 'domain', 'email_address', 'event_name', 'full_name', 'host', 'realm', 'resource', 'src_ip', 'src_port', 'src_translated_ip', 'time', 'user'] |
| edit_regex_field | host |  | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d\d:\d\d)\s({dest_host}({host}[\w\-.]+))\sPulseSecure:', '\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d\s+({dest_host}({host}[\w\-.]+))\s\d'] |
| edit_regex_field | time |  | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d\d:\d\d)\s({dest_host}({host}[\w\-.]+))\sPulseSecure:'] |
| added_regex_field | dest_host |  | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d\d:\d\d)\s({dest_host}({host}[\w\-.]+))\sPulseSecure:', '\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d\s+({dest_host}({host}[\w\-.]+))\s\d'] |
| removed_attribute | DupFields |  | N/A |