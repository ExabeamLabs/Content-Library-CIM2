# Code Changes for ruckus-r-kv-app-activity-success-filecatchsync (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| removed_parser | N/A | {"Name": "ruckus-r-kv-app-activity-success-filecatchsync", "Vendor": "Ruckus", "Product": "Ruckus", "ParserVersion": "v1.0.0", "TimeFormat": "yyyy-MM-dd HH:mm:ss", "Conditions": [":FileCache synced"], "Fields": ["({event_name}FileCache synced)", "pid=({process_id}[^,]+)"]} | N/A |