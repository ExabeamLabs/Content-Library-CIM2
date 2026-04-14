# Code Changes for microsoft-evsecurity-cef-peripheral-storage-insert-success-6416 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'channel', 'class_id', 'class_name', 'device_description', 'device_id', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'operation', 'provider_name', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['channel="({channel}[^"]+)'] |