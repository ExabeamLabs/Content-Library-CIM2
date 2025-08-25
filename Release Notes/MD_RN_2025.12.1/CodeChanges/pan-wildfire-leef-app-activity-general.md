# Code Changes for pan-wildfire-leef-app-activity-general (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| removed_parser | N/A | {"Name": "pan-wildfire-leef-app-activity-general", "Vendor": "Palo Alto Networks", "Product": "Palo Alto WildFire", "ParserVersion": "v1.0.0", "TimeFormat": "yyyy-MM-dd'T'HH:mm:ss.SSSZ", "Conditions": ["|Palo Alto Networks|PAN-OS", "ubtype=general|"], "Fields": ["ReceiveTime=({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)", "\|DeviceName=({host}[^\|]+?)\s*(\||$|\")", "\|msg=\"*({event_name}[^\|\"]+)", "\|Severity=({alert_severity}[^\|]+)", "((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"]} | N/A |