# Code Changes for github-g-csv-app-activity-success-hookcreate (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| added_parser | N/A | N/A | {"Vendor": "GitHub", "Product": "GitHub", "TimeFormat": "epoch", "Fields": ["({operation}[^,]+),({user}[\w\.\-\!\#\^\~]{1,40}\$?),(?:\s*|({resource}[^,]*)),[^,]*,(?:\s*|({object}[^,]*)),({time}\d{13}),[^,]*,(?:\s*|(\"*\[)?({additional_info_2}[^\[\]]*)(\]\"*)?),([^,]*,){3}(?:\s*|({additional_info_1}.*?))\s*$"], "Name": "github-g-csv-app-activity-success-hookcreate", "Conditions": ["hook.create,"], "ParserVersion": "v1.0.0"} |