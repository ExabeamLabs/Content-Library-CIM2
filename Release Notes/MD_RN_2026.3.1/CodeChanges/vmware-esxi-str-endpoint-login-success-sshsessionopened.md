# Code Changes for vmware-esxi-str-endpoint-login-success-sshsessionopened (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| COULD_NOT_COMPARE | TimeFormat |  | ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", 'MMM dd HH:mm:ss', 'MMM  d HH:mm:ss'] |
| changed | Conditions |  | [' vobd', '.ssh.session.opened] ', 'Correlator]', "SSH session was opened for '"] |
| edit_regex_field | additional_info |  | ['\[({additional_info}[^\]]+)\]\s*({event_name}SSH session was opened)'] |
| edit_regex_field | event_name |  | ['\[({additional_info}[^\]]+)\]\s*({event_name}SSH session was opened)'] |
| edit_regex_field | host |  | ['({time}((\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3}Z)|(\w+\s*\d+\s*\d\d:\d\d:\d\d)))\s({host}[\w\-\.]+)\s* vobd(:|\[)'] |
| edit_regex_field | time |  | ['({time}((\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3}Z)|(\w+\s*\d+\s*\d\d:\d\d:\d\d)))\s({host}[\w\-\.]+)\s* vobd(:|\[)'] |