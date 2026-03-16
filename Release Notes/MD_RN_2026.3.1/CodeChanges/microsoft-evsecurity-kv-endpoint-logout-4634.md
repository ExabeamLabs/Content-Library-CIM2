# Code Changes for microsoft-evsecurity-kv-endpoint-logout-4634 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['Computer(Name)?\s*\\*"?(=|:|>)\s*"*(::ffff:)?(am|pm|({host}[\w\.-]+))(\s|,|"|</Computer>|$)', 'Microsoft-Windows-Security-Auditing.*?({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s+(::ffff:)?(am|pm|\d{4}|({host}[\w.\-]+))\s', '\s({host}[\w.-]+)\s+Logoff\s+An account was logged off', '\w+\s*\d+\s*\d+:\d+:\d+\s+(::ffff:)?(am|pm|\d{4}|({host}[\w\-.]+))\s'] |