# Code Changes for sap-s-kv-network-session-functioncall (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| removed_parser | N/A | {"Vendor": "SAP", "Product": "SAP", "TimeFormat": "yyyy/MM/dd HH:mm:ss", "Fields": ["({time}\d\d\d\d\/\d\d\/\d\d\s\d\d:\d\d:\d\d)", "Location:\s+({host}[^\s]+)", "User:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)", "Descr:\s+({event_name}[^.]+)", "- SAP:\s+({activity_id}[^\s]+)", "({result}Successful|successful|failed|Failed)"], "Name": "sap-s-kv-network-session-functioncall", "Conditions": [" - SAP: ", " - SAP Audit ", " - SAP User: ", "Audit Class: RFC Function Call", ": Successful RFC call."], "ParserVersion": "v1.0.0"} | N/A |