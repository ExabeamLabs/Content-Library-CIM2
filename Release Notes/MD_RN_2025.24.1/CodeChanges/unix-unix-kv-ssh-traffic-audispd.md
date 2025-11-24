# Code Changes for unix-unix-kv-ssh-traffic-audispd (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_host |  | ['\s({host}({dest_host}[\w\-.]+))\s+audispd:', '\snode=({host}({dest_host}[\w\.-]+))\s'] |
| edit_regex_field | host |  | ['\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?', '\s({host}({dest_host}[\w\-.]+))\s+audispd:', '\snode=({host}({dest_host}[\w\.-]+))\s'] |
| removed_attribute | DupFields |  | N/A |