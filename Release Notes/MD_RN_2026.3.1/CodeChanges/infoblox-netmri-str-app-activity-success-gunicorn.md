# Code Changes for infoblox-netmri-str-app-activity-success-gunicorn (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| added_parser | N/A |  | {"Name": "infoblox-netmri-str-app-activity-success-gunicorn", "ParserVersion": "v1.0.0", "Vendor": "Infoblox", "Product": "Infoblox NetMRI", "TimeFormat": "MMM dd HH:mm:ss", "Conditions": [" gunicorn: ni:"], "Fields": ["({time}\w+\s\d+\s\d+:\d+:\d+)\s({host}[\w\-\.]+)\sgunicorn:\s*ni:({process_name}[^\[]+)\[({process_id}\d+)\]:\s*({operation}[^:]+):\s*({additional_info}[\s\S]+?)$", "(Processing path|found for|from remote host\s*\")\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"]} |