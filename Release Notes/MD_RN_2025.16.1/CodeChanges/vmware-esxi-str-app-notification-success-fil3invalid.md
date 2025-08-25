# Code Changes for vmware-esxi-str-app-notification-success-fil3invalid (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| added_parser | N/A |  | {"Vendor": "VMware", "Product": "VMware ESXi", "TimeFormat": "yyyy-MM-dd'T'HH:mm:ss.SSSZ", "Fields": ["({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}Z)", "\d\d:\d\d:\d\d\.\d{1,3}Z\s({host}[^\s]+)", "storageRM\[[^\]]+\]:\s*({additional_info}[^$]+?)\s*$", "WARNING:(\s*[^:]+:){2}\s*({additional_info}[^$]+?)\s*$"], "Name": "vmware-esxi-str-app-notification-success-fil3invalid", "ParserVersion": "v1.0.0", "Conditions": [": Found invalid object on ", ")WARNING: ", " Fil3: "]} |