# Code Changes for unix-ad-kv-endpoint-notification-netfiltercfg (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({dest_host}({host}[\w.\-]+))))\s+(\d\S+|tag_audit_log({=dest_host}({=host}[\w.\-]+))\s)?', '\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z\s({host}[\w\-.]+)\saudit'] |