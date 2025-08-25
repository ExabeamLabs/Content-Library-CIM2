# Code Changes for sensormatik-s-cef-physical-location-access-success-sensormatik (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| removed_parser | N/A | {"Name": "sensormatik-s-cef-physical-location-access-success-sensormatik", "Vendor": "Sensormatik", "Product": "Sensormatik", "TimeFormat": "epoch", "Conditions": ["|Sensormatik|", "suser="], "Fields": ["([^\|]*\|){5}({result}[^\|]+)", "\Wrt=({time}\d{13})", "\Wsuser=({last_name}[^,]+), ({first_name}[^\s]+)\s(\d+|\w+=)", "\Wcs3=({location_door}.+?)\s*(\w+=|$)", "\Wcs2=({direction}.+?)\s*(\w+=|$)"], "ParserVersion": "v1.0.0"} | N/A |