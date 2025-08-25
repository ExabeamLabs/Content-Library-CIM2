# Code Changes for postscript-ps-str-printer-activity-success-print (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| removed_parser | N/A | {"Name": "postscript-ps-str-printer-activity-success-print", "Vendor": "PostScript", "Product": "PostScript", "TimeFormat": "yyyy-MM-dd  HH:- mm:ss a", "Conditions": [" PostScript  PRINT"], "Fields": ["({time}\d+\-\d+\-\d+\s+\d+:\-\s*\d+:\d+ (PM|pm|AM|am))\s+({host}[^\s]+)\s+(?:-|({printer_name}[^\s]+))\s+(?:-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\S+\s+(?:-|({src_host}[^\s]+))\s+(?:-|({object}.+?))\s+(\d+\s+){3}\d+\.\d+\s+.+?\s+(\d+\s+){3}PostScript  ({operation}PRINT)"], "DupFields": ["printer_name->dest_host"], "ParserVersion": "v1.0.0"} | N/A |