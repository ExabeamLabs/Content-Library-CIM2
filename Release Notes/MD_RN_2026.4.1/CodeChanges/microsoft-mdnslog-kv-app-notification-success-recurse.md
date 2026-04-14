# Code Changes for microsoft-mdnslog-kv-app-notification-success-recurse (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| added_parser | N/A |  | {"Name": "microsoft-mdnslog-kv-app-notification-success-recurse", "Vendor": "Microsoft", "Product": "Microsoft DNS Log", "TimeFormat": ["M/d/yyyy HH:mm:ss a", "MM/dd/yyyy HH:mm:ss a"], "Conditions": [" RECURSE "], "ParserVersion": "v1.0.0", "Fields": ["({time}\d{1,2}\/\d{1,2}\/\d\d\d\d\s\d{1,2}:\d\d:\d\d\s(am|AM|PM|pm))", "({event_name}RECURSE)\s+({additional_info}.+?)$"]} |