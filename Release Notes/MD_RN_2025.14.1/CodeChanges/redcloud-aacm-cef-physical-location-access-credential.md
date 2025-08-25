# Code Changes for redcloud-aacm-cef-physical-location-access-credential (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| removed_parser | N/A | {"Name": "redcloud-aacm-cef-physical-location-access-credential", "Vendor": "Aviglion", "Product": "Aviglion ACM", "TimeFormat": "epoch", "Conditions": ["CEF:", "|RedCloud|Enterprise|", "Credential"], "Fields": ["\srt=({time}\d{13})", "\|(?:([^\|]*\|)){4}({action}[^\|]+)", "\scat=({category}.+?)\s+\w+=", "\sduser=({last_name}[^,]+),({first_name}.+?)\s+\w+=", "\scs1=({location_building}.+?)\s+\w+=", "\scs5=({location_door}.+?)\s+\w+="], "ParserVersion": "v1.0.0"} | N/A |