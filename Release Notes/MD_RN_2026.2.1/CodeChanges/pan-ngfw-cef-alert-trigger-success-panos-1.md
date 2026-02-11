# Code Changes for pan-ngfw-cef-alert-trigger-success-panos-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | device_name |  | ['\sdvchost=({device_name}[^=]+)\s\w+='] |
| edit_regex_field | host |  | ['\s(-|({host}[\w\-.]+?))\sCEF:', '\sdvchost=({host}[\w\-.]+)\s\w+='] |