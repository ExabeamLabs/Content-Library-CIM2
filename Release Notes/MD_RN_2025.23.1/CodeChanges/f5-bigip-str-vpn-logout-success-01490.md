# Code Changes for f5-bigip-str-vpn-logout-success-01490 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_host |  | ['"host":\{"name":"({dest_host}({host}[\w\-\.]+))', '\d\d:\d\d\s+({dest_host}({host}[^\s]+))\s([^\s]+\s)?[^\s]+\[\d+\]', '\w+\s\d+\s\d\d:\d\d:\d\d\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s({dest_host}[\w\-.]+)', 'hostname="({dest_host}({host}[\w\-\.]+))'] |
| edit_regex_field | host |  | ['"host":\{"name":"({dest_host}({host}[\w\-\.]+))', '\d\d:\d\d\s+({dest_host}({host}[^\s]+))\s([^\s]+\s)?[^\s]+\[\d+\]', 'hostname="({dest_host}({host}[\w\-\.]+))'] |
| removed_attribute | DupFields |  | N/A |