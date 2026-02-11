# Code Changes for cisco-asa-kv-network-session-fail-750003 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | event_name |  | ['Username:(\d{1,3}(\.\d{1,3}){3}|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+({protocol}\w+)?\s*({event_name}Negotiation aborted due to ERROR)'] |
| edit_regex_field | protocol |  | ['Username:(\d{1,3}(\.\d{1,3}){3}|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+({protocol}\w+)?\s*({event_name}Negotiation aborted due to ERROR)'] |
| edit_regex_field | user |  | ['Username:(\d{1,3}(\.\d{1,3}){3}|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+({protocol}\w+)?\s*({event_name}Negotiation aborted due to ERROR)'] |