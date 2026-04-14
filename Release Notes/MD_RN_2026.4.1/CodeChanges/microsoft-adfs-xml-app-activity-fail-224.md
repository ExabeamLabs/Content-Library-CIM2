# Code Changes for microsoft-adfs-xml-app-activity-fail-224 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'event_code', 'host', 'new_hash', 'time'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<\/Channel>'] |