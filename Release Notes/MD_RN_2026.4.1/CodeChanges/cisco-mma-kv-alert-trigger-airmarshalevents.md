# Code Changes for cisco-mma-kv-alert-trigger-airmarshalevents (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['({time}\d{10})\.\d*\s+({host}[\w.\-]+)\s+({alert_name}[^=]+?)\s+type=({alert_type}({event_name}.+?))\s+\w+=', '\d\d:\d\d:\d\d\s*({host}[\w.-]+)\s'] |