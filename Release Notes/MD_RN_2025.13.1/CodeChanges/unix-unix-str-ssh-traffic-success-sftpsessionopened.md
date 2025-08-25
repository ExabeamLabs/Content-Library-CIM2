# Code Changes for unix-unix-str-ssh-traffic-success-sftpsessionopened (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| COULD_NOT_COMPARE | TimeFormat |  | ['yyyy-MM-dd HH:mm:ss', 'MMM dd HH:mm:ss'] |
| changed_parsed_fields | N/A |  | ['event_name', 'host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | host |  | ['({time}\w+\s+\d+\s+\d+:\d+:\d+)\s*({host}[\w.\-]+) \S*sftp'] |
| added_regex_field | time |  | ['({time}\w+\s+\d+\s+\d+:\d+:\d+)\s*({host}[\w.\-]+) \S*sftp'] |
| changed | Conditions |  | [' session opened ', ']: ', 'sftp'] |