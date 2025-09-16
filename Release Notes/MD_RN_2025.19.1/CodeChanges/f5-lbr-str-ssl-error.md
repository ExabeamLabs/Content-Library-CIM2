# Code Changes for f5-lbr-str-ssl-error (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| added_parser | N/A |  | {"Name": "f5-lbr-str-ssl-error", "ParserVersion": "v1.0.0", "Vendor": "F5", "Product": "BIG-IP F5 LBR", "TimeFormat": ["MMM dd HH:mm:ss", "MMM  d HH:mm:ss"], "Conditions": [": SSL", "big3d"], "Fields": ["({time}\w+\s+\d+ \d+:\d+:\d+)\s+({host}[^\s]+)\s+({severity}[^\s]+)\s+({process_name}[^\[]+)\[\d+\]:\s*({event_code}[^\:]+):\d+:\s*({additional_info}.+$)", "({failure_reason}(certificate verify failed|SSL cert EXPIRED|SSL error during shutdown))", "::ffff:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"]} |