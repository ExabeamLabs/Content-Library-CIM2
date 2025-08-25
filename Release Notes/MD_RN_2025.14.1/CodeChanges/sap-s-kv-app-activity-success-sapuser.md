# Code Changes for sap-s-kv-app-activity-success-sapuser (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| removed_parser | N/A | {"Vendor": "SAP", "Product": "SAP", "TimeFormat": "yyyy/MM/dd HH:mm:ss", "Fields": ["({time}\d\d\d\d\/\d\d\/\d\d\s\d\d:\d\d:\d\d)", "Location:\s+({host}[^\s]+)", "User:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)", "Descr:\s+({event_name}[^.]+)", "- SAP:\s+({activity_id}[^\s]+)", "({result}Successful|successful|failed|Failed)", "({app}SAP)"], "Name": "sap-s-kv-app-activity-success-sapuser", "Conditions": [" - SAP: ", " - SAP Audit ", " - SAP User: ", "Audit Class: "], "DupFields": ["event_name->operation"], "ParserVersion": "v1.0.0"} | N/A |