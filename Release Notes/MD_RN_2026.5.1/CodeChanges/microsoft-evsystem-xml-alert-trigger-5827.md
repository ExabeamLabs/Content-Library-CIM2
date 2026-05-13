# Code Changes for microsoft-evsystem-xml-alert-trigger-5827 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_severity', 'channel', 'domain', 'event_code', 'event_id', 'host', 'os', 'provider_name', 'result', 'run_level', 'time', 'user_type'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |