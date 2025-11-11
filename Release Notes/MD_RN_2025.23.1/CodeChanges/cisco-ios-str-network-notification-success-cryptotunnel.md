# Code Changes for cisco-ios-str-network-notification-success-cryptotunnel (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| added_parser | N/A |  | {"Name": "cisco-ios-str-network-notification-success-cryptotunnel", "Vendor": "Cisco", "Product": "Cisco IOS", "TimeFormat": "MMM dd yyyy HH:mm:ss", "Conditions": ["%CRYPTO-5-IKEV2_SESSION_STATUS:", "Crypto tunnel"], "Fields": ["({time}\w+\s+\d+\s+\d+\s+\d\d:\d\d:\d\d)", "({event_category}%[^:\s]+):", "({event_name}Crypto tunnel v2 is (UP|DOWN))", "Peer\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"], "ParserVersion": "v1.0.0"} |