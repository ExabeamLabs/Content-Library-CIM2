# Code Changes for cisco-gateway-str-group-member-add-success-confd (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| added_parser | N/A |  | {"Name": "cisco-gateway-str-group-member-add-success-confd", "Vendor": "Cisco", "Product": "Cisco Collaboration", "TimeFormat": "yyyy-MM-dd'T'HH:mm:ssz", "Conditions": [" confd ", " audit user: ", " assigned to groups:"], "Fields": ["({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d[+-]\d\d:\d\d)", ":\d\d:\d\d[+-]\d\d:\d\d\s({host}[\w.-]+)", "\s({process_name}confd)\s+({process_id}[^\s]+)", "audit ({event_name}user:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\/({user_id}[^\s]+) assigned to groups:\s*({additional_info}({group_name}[^\s\",]+)[^\"]*))"], "ParserVersion": "v1.0.0"} |