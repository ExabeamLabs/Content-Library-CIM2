# Code Changes for unix-unixdhcpd-str-dhcp-session-success-dhcpd (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| added_parser | N/A | N/A | {"Name": "unix-unixdhcpd-str-dhcp-session-success-dhcpd", "Vendor": "Unix", "Product": "Unix dhcpd", "TimeFormat": "yyyy-MM-dd HH:mm:ss", "Conditions": [" dhcpd: ", " Forward map from "], "Fields": ["\d\d:\d\d:\d\d\s+({host}.+?)\s+dhcpd: Forward map from ({dest_host}[^\s]+) to ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s+({additional_info}.+?)\.\s*(\w+=|'|\"|$)"], "DupFields": ["dest_host->user"], "ParserVersion": "v1.0.0"} |