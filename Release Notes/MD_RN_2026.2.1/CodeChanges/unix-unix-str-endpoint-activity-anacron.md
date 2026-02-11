# Code Changes for unix-unix-str-endpoint-activity-anacron (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['\d\d:\d\d:\d\d\s*({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})?\s*(\d+|({host}[\w\-\.]+))\s+(({event_category}[^\s]+)\s+)?anacron', '\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d*\s+|tag_audit_log|(\d+|({host}[\w.\-]+))))\s+(\d*\S+|tag_audit_log|(\d+|({=host}[\w.\-]+))\s)?'] |
| edit_regex_field | host_ip |  | ['\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d*\s+|tag_audit_log|(\d+|({host}[\w.\-]+))))\s+(\d*\S+|tag_audit_log|(\d+|({=host}[\w.\-]+))\s)?'] |