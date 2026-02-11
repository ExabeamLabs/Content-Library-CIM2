# Code Changes for cisco-asa-str-network-notification-bgp (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | event_code |  | ['({event_code}%BGP-[^:]+)', '({event_code}%\w+\-[^:\s]+):'] |