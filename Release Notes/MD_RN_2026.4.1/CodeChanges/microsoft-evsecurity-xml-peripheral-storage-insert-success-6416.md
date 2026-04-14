# Code Changes for microsoft-evsecurity-xml-peripheral-storage-insert-success-6416 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'dest_host', 'device_class', 'device_description', 'device_id', 'device_pid', 'device_vid', 'domain', 'event_code', 'event_name', 'operation', 'run_level', 'time', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |