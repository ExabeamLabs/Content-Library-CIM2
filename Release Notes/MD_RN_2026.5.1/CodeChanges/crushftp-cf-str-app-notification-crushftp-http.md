# Code Changes for crushftp-cf-str-app-notification-crushftp-http (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| added_parser | N/A |  | {"Name": "crushftp-cf-str-app-notification-crushftp-http", "Vendor": "CrushFTP", "Product": "CrushFTP", "ParserVersion": "v1.0.0", "TimeFormat": "MM/dd/yyyy HH:mm:ss.SSS", "Conditions": ["crushftp", "SFTPNA_BE.log:"], "Fields": ["\|({time}\d{2}\/\d{2}\/\d{4}\s\d{2}:\d{2}:\d{2}\.\d{3})\|({additional_info}.*)$", "\d+:\d+:\d+\s+({host}[\w\-\.]+)\s"]} |