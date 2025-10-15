# Code Changes for postfix-postfix-str-smtp-close-connectionfail (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| added_parser | N/A |  | {"Name": "postfix-postfix-str-smtp-close-connectionfail", "Vendor": "Postfix", "Product": "Postfix", "TimeFormat": ["MMM dd HH:mm:ss"], "Conditions": ["postfix", "]: connect to", "]:"], "Fields": ["({time}\w\w\w \d\d \d\d:\d\d:\d\d)\s({host}[\w\-\.]+)\s({process_name}[^\[]+)\[({process_id}[^\]]+)]\s*({message_id}[\w]+)", "\Wconnect to\s+({dest_host}[\w\-.]+)\[({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))?\]:({dest_port}\d+)?:\s*({additional_info}[^$]+)"], "ParserVersion": "v1.0.0"} |