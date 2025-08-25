# Code Changes for sensormatik-s-kv-physical-location-access-cardadmitted (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| removed_parser | N/A | {"Name": "sensormatik-s-kv-physical-location-access-cardadmitted", "ParserVersion": "v1.0.0", "Vendor": "Sensormatik", "Product": "Sensormatik", "TimeFormat": "yyyy-MM-dd HH:mm:ss", "Conditions": ["Sensormatik_PersonalLog", "Door=\"", "Direction="], "Fields": ["Status=\"+({result}[^\"]+)\"", "Date=\"+({time}[^\"\.]+)", "Id=\"+({badge_id}\d+)\"", "Personnel=\"+({last_name}[^,]+), ({first_name}[^\"]+)\"", "Door=\"+({location_door}[^\"]+)\"", "Direction=\"+({direction}[^\"]+)\"", "Text1=\"+({additional_info}[^\"]+)\""]} | N/A |