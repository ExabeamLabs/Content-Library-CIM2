# Code Changes for pan-gp-cef-app-activity-success-globalprotect (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | device_name |  | [',GLOBALPROTECT,([^,]*,){44}(\d|({device_name}({host}[\w\-\.]+))),', ',GLOBALPROTECT,([^,]*,){48}(\d|({device_name}({host}[^,]+)))'] |
| edit_regex_field | event_category |  | [',({event_category}SYSTEM|TRAFFIC)'] |
| edit_regex_field | host |  | [',GLOBALPROTECT,([^,]*,){44}(\d|({device_name}({host}[\w\-\.]+))),', ',GLOBALPROTECT,([^,]*,){48}(\d|({device_name}({host}[^,]+)))', ':\d\d:\d\d\s+({host}[\w.-]+)\s', '\d+:\d+:\d\d[\+-]\d+:\d+\s+({host}[\w.-]+)\s', '\d\d:\d\d:\d\d\s({host}[\w\-\.]+)\s*\d*,({time}\d\d\d\d\/\d\d\/\d\d\s\d\d:\d\d:\d\d),'] |
| edit_regex_field | time |  | ['((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))', '({time}\d\d\d\d\/\d\d\/\d\d\s\d\d:\d\d:\d\d)', ',GLOBALPROTECT,([^,]+,){2}({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z),', '\d\d:\d\d:\d\d\s({host}[\w\-\.]+)\s*\d*,({time}\d\d\d\d\/\d\d\/\d\d\s\d\d:\d\d:\d\d),'] |