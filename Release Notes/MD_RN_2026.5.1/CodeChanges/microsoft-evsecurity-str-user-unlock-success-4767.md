# Code Changes for microsoft-evsecurity-str-user-unlock-success-4767 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['(success|failure|audit)\s+\w+\s+(::ffff:)?({host}[\w\-.]+)', 'Computer(Name)?\s*\\*\"?(=|:|>)\s*\"*(::ffff:)?({host}[\w\.-]+)(\s|,|\"|</Computer>|$)', '\w+\s*\d+\s\d+:\d+:\d+\s+(::ffff:)?(am|pm|\d{4}|({host}[\w\-.]+))\s\w'] |