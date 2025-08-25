# Code Changes for citrix-cgateway-str-app-authentication-message (Parser)

| Code Change | Field Name | 2025.14.1 | 2025.15.1 |
|-------------|------------|-----------|------------|
| removed_parser | N/A | {"Name": "citrix-cgateway-str-app-authentication-message", "ParserVersion": "v1.0.0", "Vendor": "Citrix", "Product": "Citrix Gateway", "TimeFormat": "MM/dd/yyyy:HH:mm:ss", "Conditions": [" AAA Message ", "In receive_ldap_user_bind_event"], "Fields": ["({time}\d+\/\d+\/\d+:\d+:\d+:\d+)\s*GMT", "GMT\s*({host}[^:\s]+)(\s\S+)?\s:\s*({event_code}(\w+\s+){3})[^:]+:\s*\"*\s*({additional_info}[^\"]+)\"*"], "DupFields": ["host->src_host"]} | N/A |