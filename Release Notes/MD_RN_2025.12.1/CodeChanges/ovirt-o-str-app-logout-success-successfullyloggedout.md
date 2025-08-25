# Code Changes for ovirt-o-str-app-logout-success-successfullyloggedout (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| removed_parser | N/A | {"Name": "ovirt-o-str-app-logout-success-successfullyloggedout", "Vendor": "oVirt", "Product": "oVirt", "ParserVersion": "v1.0.0", "TimeFormat": "yyyy-MM-dd HH:mm:ss", "Conditions": ["INFO", "ovirt", "successfully logged out"], "Fields": ["({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),.+?ovirt", "User (?:({email_address}[^\s@]+@[^\s@]+)\S*|({user}[\w\.\-\!\#\^\~]{1,40}\$?)) successfully logged out"]} | N/A |