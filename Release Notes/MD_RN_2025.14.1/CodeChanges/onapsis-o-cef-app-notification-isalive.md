# Code Changes for onapsis-o-cef-app-notification-isalive (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| added_parser | N/A | N/A | {"Name": "onapsis-o-cef-app-notification-isalive", "Product": "Onapsis", "Vendor": "Onapsis", "ParserVersion": "v1.0.0", "TimeFormat": "MMM dd yyyy HH:mm:ss", "Conditions": ["CEF:", "|Onapsis|OSP|", "|Is Alive|"], "Fields": ["\Wend=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)", "\Wevent_id=({event_name}.+?)(\s+\w+=|\s*$)"]} |