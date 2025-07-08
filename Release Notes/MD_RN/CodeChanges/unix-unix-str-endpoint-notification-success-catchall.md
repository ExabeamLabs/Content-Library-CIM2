# Code Changes for unix-unix-str-endpoint-notification-success-catchall (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| added_parser | N/A | N/A | {"Name": "unix-unix-str-endpoint-notification-success-catchall", "ParserVersion": "v1.0.0", "Conditions": [" rsyslogd[", "]: "], "Vendor": "Unix", "Product": "Unix", "TimeFormat": ["epoch_sec", "MMM dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"], "Fields": ["action\s'({action}[^'\s]+)'", "\srsyslogd\[\d+\]:\s*({additional_info}.+?)\s*$"]} |