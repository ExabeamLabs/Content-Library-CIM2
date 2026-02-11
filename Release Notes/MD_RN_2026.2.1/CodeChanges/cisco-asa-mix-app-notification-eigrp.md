# Code Changes for cisco-asa-mix-app-notification-eigrp (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | event_code |  | ['({event_code}%\w+\-[^:\s]+):', 'ad.mnemonic=({event_code}.*?)\sad.message'] |