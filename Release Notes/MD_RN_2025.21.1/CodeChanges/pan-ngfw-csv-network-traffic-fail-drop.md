# Code Changes for pan-ngfw-csv-network-traffic-fail-drop (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_country |  | [',TRAFFIC,([^,]*,){38}({dest_country}[^\.:\d,]+?)\s*,'] |
| edit_regex_field | host |  | [',TRAFFIC,([^,]*,){48}({device_name}({host}[\w.-]+))'] |
| edit_regex_field | src_country |  | [',TRAFFIC,([^,]*,){37}({src_country}[^\.:\d,]+?)\s*,'] |
| edit_regex_field | time |  | [',((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+)),', ',({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d),', ',TRAFFIC,([^,]*,){2}({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)', ',TRAFFIC,([^,]*,){2}({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+)'] |