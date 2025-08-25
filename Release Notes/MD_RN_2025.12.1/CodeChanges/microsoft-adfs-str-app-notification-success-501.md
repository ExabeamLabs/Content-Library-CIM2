# Code Changes for microsoft-adfs-str-app-notification-success-501 (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| removed_parser | N/A | {"Name": "microsoft-adfs-str-app-notification-success-501", "ParserVersion": "v1.0.0", "Vendor": "Microsoft", "Product": "Active Directory Federation Services", "TimeFormat": "yyyy-MM-dd HH:mm:ss", "Conditions": [" AD_FS_Auditing[", " AUDIT_FAILURE 501 "], "Fields": ["({host}[\w\-.]+)\s+AD_FS_Auditing\[\d+\]:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)", "AUDIT_FAILURE\s+({event_code}\d+)\s+(({domain}[^\\\s]+)\\+)?({service_name}[^\\\s]+)\s+({failure_reason}[^\.]+?)\."]} | N/A |