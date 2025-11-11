# Code Changes for juniper-ps-mix-vpn-login-success-passed (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'email_address', 'host', 'realm', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | time |  | ['PulseSecure:.+?({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)\s+\-\s+({dest_host}[\w\-.]+)', 'PulseSecure:.+?({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)\s+\-\s+({host}[\w\-.]+)', 'PulseSecure:\s+({time}\d\d\d\d\-\d\d-\d\d \d\d:\d\d:\d\d)'] |
| added_regex_field | dest_host |  | ['PulseSecure:.+?({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)\s+\-\s+({dest_host}[\w\-.]+)'] |
| removed_attribute | DupFields |  | N/A |