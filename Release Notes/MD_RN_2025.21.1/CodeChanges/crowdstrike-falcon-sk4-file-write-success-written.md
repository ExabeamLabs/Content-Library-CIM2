# Code Changes for crowdstrike-falcon-sk4-file-write-success-written (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['aid', 'bytes', 'cid', 'device_id', 'email_address', 'event_code', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'first_name', 'full_name', 'last_name', 'os', 'service_type', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | device_id |  | ['"DiskParentDeviceInstanceId":"({service_type}({device_id}[^"]{1,2099}))"'] |
| added_regex_field | service_type |  | ['"DiskParentDeviceInstanceId":"({service_type}({device_id}[^"]{1,2099}))"'] |
| removed_attribute | DupFields |  | N/A |