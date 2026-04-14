# Code Changes for microsoft-evsecurity-xml-ds-object-activity-success-4662 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'access_list', 'access_mask', 'channel', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'object_name', 'object_server', 'object_type', 'operation', 'properties', 'result', 'run_level', 'src_domain', 'src_host', 'src_user', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |