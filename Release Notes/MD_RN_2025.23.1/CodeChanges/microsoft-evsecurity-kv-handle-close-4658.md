# Code Changes for microsoft-evsecurity-kv-handle-close-4658 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_host |  | ['"(?i)HostName":\s*"({dest_host}({host}[^"]+))"', '(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(::ffff:)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(am|pm|\d{4}|({dest_host}[\w\-.]+)))\s', '\d+\s*\d+:\d+:\d+\s+(::ffff:)?(am|pm|\d{4}|({dest_host}({host}[\w\-.]+)))\s'] |
| edit_regex_field | host |  | ['"(?i)HostName":\s*"({dest_host}({host}[^"]+))"', '\d+\s*\d+:\d+:\d+\s+(::ffff:)?(am|pm|\d{4}|({dest_host}({host}[\w\-.]+)))\s'] |
| removed_attribute | DupFields |  | N/A |