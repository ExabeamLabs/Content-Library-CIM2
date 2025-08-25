# Code Changes for vmware-horizon-str-endpoint-authentication-success-requestedpool (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| added_parser | N/A |  | {"Name": "vmware-horizon-str-endpoint-authentication-success-requestedpool", "ParserVersion": "v1.0.0", "Vendor": "VMware", "Product": "VMware Horizon", "TimeFormat": "yyyy-MM-dd HH:mm:ss", "Conditions": [" View ", "requested Pool "], "Fields": ["\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)", "({app}View)", "User\s+(({domain}[^\\\s]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)", "({event_name}({operation}requested Pool (nuvdmpool|melzerpool)(-gpu|-nu)?).*?)\s+$", "({event_name}({operation}requested Pool [^,]+?)(,[^\"]*?)?)[\s\"]*$", " machine\s+({dest_host}[\w\-.]+)"]} |