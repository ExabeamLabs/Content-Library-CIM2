# Code Changes for juniper-ps-str-vpn-logout-success-loggedout (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'email_address', 'host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | dest_host |  | ['\s({host}({dest_host}[^\s]+))\s+PulseSecure:'] |
| added_regex_field | host |  | ['\s({host}({dest_host}[^\s]+))\s+PulseSecure:'] |
| removed_attribute | DupFields |  | N/A |