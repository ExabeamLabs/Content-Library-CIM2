# Code Changes for pan-ngfw-str-alert-trigger-success-paseries (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| removed_parser | N/A | {"Name": "pan-ngfw-str-alert-trigger-success-paseries", "Vendor": "Palo Alto Networks", "Product": "Palo Alto NGFW", "TimeFormat": "yyyy-MM-dd'T'HH:mm:ss.SSSZ", "Conditions": ["A device has stopped emitting events", "'PaSeries @"], "Fields": ["'PaSeries @ ({src_host}[^\s']+)( \(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\))?'", "({alert_name}A device has stopped emitting events)", "((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"], "ParserVersion": "v1.0.0"} | N/A |