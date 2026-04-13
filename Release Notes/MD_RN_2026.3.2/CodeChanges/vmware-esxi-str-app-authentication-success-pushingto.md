# Code Changes for vmware-esxi-str-app-authentication-success-pushingto (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | additional_info |  | ['Pushing\s({additional_info}[^"]+?)\s*("|$)'] |
| edit_regex_field | host |  | ['\d\d:\d\d\s({host}[\w\-]+)\s[^\[]+'] |
| edit_regex_field | time |  | ['\[({time}\d{4}\-\d{1,2}\-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}\.\d{1,3}Z)'] |