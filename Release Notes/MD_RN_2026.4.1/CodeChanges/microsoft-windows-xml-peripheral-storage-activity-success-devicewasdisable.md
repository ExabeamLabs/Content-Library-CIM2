# Code Changes for microsoft-windows-xml-peripheral-storage-activity-success-devicewasdisable (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'dest_host', 'device_class', 'device_description', 'device_id', 'device_pid', 'device_vid', 'domain', 'event_code', 'event_name', 'operation', 'run_level', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |