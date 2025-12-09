# Code Changes for crowdstrike-falcon-json-file-write-success-written (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['aid', 'aip', 'bytes', 'device_id', 'email_address', 'email_domain', 'event_code', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'hash_sha256', 'os', 'process_guid', 'service_type', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | device_id |  | ['"DiskParentDeviceInstanceId":"({service_type}({device_id}[^"]+))"'] |
| added_regex_field | service_type |  | ['"DiskParentDeviceInstanceId":"({service_type}({device_id}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |