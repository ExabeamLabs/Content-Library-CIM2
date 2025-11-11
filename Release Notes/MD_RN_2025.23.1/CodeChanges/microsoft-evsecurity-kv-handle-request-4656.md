# Code Changes for microsoft-evsecurity-kv-handle-request-4656 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_host |  | ['(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(::ffff:)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(am|pm|\d{4}|({dest_host}[\w\-.]+)))\s', '(?i)\w+\s*\d+\s*\d\d:\d\d:\d\d (::ffff:)?(am|pm|\d{4}|({dest_host}({host}[\w\-.]+)))\s', 'Computer(Name)?\s*\\*"?(=|:|>)\s*"*(::ffff:)?({dest_host}({host}[\w\.-]+))(\s|,|"|</Computer>|$)'] |
| edit_regex_field | host |  | ['(?i)\w+\s*\d+\s*\d\d:\d\d:\d\d (::ffff:)?(am|pm|\d{4}|({dest_host}({host}[\w\-.]+)))\s', 'Computer(Name)?\s*\\*"?(=|:|>)\s*"*(::ffff:)?({dest_host}({host}[\w\.-]+))(\s|,|"|</Computer>|$)'] |
| removed_attribute | DupFields |  | N/A |