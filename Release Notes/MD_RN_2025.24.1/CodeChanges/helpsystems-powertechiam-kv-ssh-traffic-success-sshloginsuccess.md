# Code Changes for helpsystems-powertechiam-kv-ssh-traffic-success-sshloginsuccess (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth', 'dest_host', 'event_code', 'host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | host |  | ['\d\dZ\s+({dest_host}({host}[\w\-.]+))\s+sshd - sshlogin'] |
| added_regex_field | dest_host |  | ['\d\dZ\s+({dest_host}({host}[\w\-.]+))\s+sshd - sshlogin'] |
| removed_attribute | DupFields |  | N/A |