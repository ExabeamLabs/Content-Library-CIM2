# Code Changes for int64software-ol-str-user-password-read-success-readthepassword (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| added_parser | N/A |  | {"Name": "int64software-ol-str-user-password-read-success-readthepassword", "Vendor": "Int64 Software", "Product": "OVERLAPS", "TimeFormat": "dd/MM/yy HH:mm:ss.SSS", "Conditions": ["Read the password for the computer", "(User:"], "Fields": ["({time}\d\d\/\d\d\/\d\d\s+\d\d:\d\d:\d\d.\d\d\d)", "\s+\[({severity}\w+)\s+\]\s+", "({event_name}Read the password)", "<\w+>({src_host}[\w\-\.]+)<\/\w+>\s+in\s+({resource_path}[^\s\(]+?)\.\s+\(", "\(User:\s+\[({user_id}\d+)\]\s+({domain}[^\/]+)\/({user}[\w\.\-\!\#\^\~]{1,40}\$?)\)"], "ParserVersion": "v1.0.0"} |