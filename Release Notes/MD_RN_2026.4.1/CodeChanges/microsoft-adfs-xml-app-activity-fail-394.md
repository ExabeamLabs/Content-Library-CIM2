# Code Changes for microsoft-adfs-xml-app-activity-fail-394 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'event_code', 'host', 'time'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<\/Channel>'] |