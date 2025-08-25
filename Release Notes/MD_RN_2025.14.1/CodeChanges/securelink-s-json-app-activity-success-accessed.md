# Code Changes for securelink-s-json-app-activity-success-accessed (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| removed_parser | N/A | {"Name": "securelink-s-json-app-activity-success-accessed", "Vendor": "SecureLink", "Product": "SecureLink", "TimeFormat": "yyyy-MM-dd HH:mm:ss", "Conditions": ["SecureLink:", "AUDIT:", "accessed service:"], "Fields": ["Application:\s*({app}[^,]+)", "AUDIT:.+?\(({email_address}[^)]+)\)", "({operation}accessed service):\s*({object}[^,]+)", "port ({dest_port}\d+)", "duration: ({duration}\w+)"], "ParserVersion": "v1.0.0"} | N/A |