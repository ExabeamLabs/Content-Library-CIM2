# Code Changes for microsoft-evsecurity-xml-certificate-modify-success-5126 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['activity_id', 'channel', 'event_code', 'hash_sha1', 'host', 'run_level', 'time'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |