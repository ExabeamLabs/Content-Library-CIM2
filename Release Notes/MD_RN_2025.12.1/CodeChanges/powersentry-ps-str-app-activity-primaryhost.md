# Code Changes for powersentry-ps-str-app-activity-primaryhost (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| removed_parser | N/A | {"Name": "powersentry-ps-str-app-activity-primaryhost", "Vendor": "PowerSentry", "Product": "PowerSentry", "TimeFormat": "yyyy-MM-dd HH:mm:ss", "Conditions": [" [Sentry", " primary host changed to "], "Fields": ["\d\d:\d\d:\d\d ({host}[^\s]+) \[({src_host}[^\]]+)\].+? by user \"({user}[\w\.\-\!\#\^\~]{1,40}\$?)", "({operation}primary host changed)"], "ParserVersion": "v1.0.0"} | N/A |