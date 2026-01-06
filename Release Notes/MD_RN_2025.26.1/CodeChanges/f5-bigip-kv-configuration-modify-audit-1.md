# Code Changes for f5-bigip-kv-configuration-modify-audit-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| added_parser | N/A |  | {"Name": "f5-bigip-kv-configuration-modify-audit-1", "ParserVersion": "v1.0.0", "Vendor": "F5", "Product": "F5 BIG-IP", "TimeFormat": ["yyyy-MM-dd HH:mm:ss", "MMM dd HH:mm:ss"], "Conditions": [" user=", " action=", " status=", ": AUDIT "], "Fields": ["<(?:\d{1,3})>(?:\d{0,2}\s)?({time}\w{3}\s+\d{1,2}\s+\d{2}:\d{2}:\d{2})", "({host}[\w.-]+)\snotice", "\suser=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s\"\\,\|]+\.[^\]\s\"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))", "\saction=\"({action}[^\"]+)", "\sstatus=\"({status_msg}[^\"]+)"]} |