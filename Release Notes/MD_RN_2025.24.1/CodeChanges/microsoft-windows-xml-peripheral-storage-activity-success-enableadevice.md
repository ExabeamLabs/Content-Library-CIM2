# Code Changes for microsoft-windows-xml-peripheral-storage-activity-success-enableadevice (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_host', 'device_class', 'device_description', 'device_id', 'device_pid', 'device_vid', 'domain', 'event_code', 'event_name', 'operation', 'run_level', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | event_name |  | ['({operation}({event_name}A request was made to enable a device.))'] |
| added_regex_field | operation |  | ['({operation}({event_name}A request was made to enable a device.))'] |