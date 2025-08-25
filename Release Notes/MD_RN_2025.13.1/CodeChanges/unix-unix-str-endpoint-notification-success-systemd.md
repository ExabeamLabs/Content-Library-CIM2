# Code Changes for unix-unix-str-endpoint-notification-success-systemd (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions |  | [' systemd-', ': '] |
| edit_regex_field | additional_info |  | ['\ssystemd(-\w+)?(\[\d+\])?:\s*({additional_info}.+?)\s*$'] |
| edit_regex_field | host |  | ['({time}\d\d\d\d-\d+-\d+T\d\d:\d\d:\d\d\.\d+[-+]\d\d:\d\d)\s+({host}[\w.\-]+)', '({time}\w+\s+\d+\s+\d+:\d+:\d+)\s*({host}[\w\-.]+)(\s\w+)?\s*(systemd-)', '\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?'] |
| edit_regex_field | time |  | ['({time}\d\d\d\d-\d+-\d+T\d\d:\d\d:\d\d\.\d+[-+]\d\d:\d\d)\s+({host}[\w.\-]+)', '({time}\w+\s+\d+\s+\d+:\d+:\d+)\s*({host}[\w\-.]+)(\s\w+)?\s*(systemd-)'] |