# Code Changes for box-ccm-json-file-download-success-manageddevice (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access_type', 'additional_info', 'bytes', 'dest_host', 'dest_ip', 'device_id', 'device_name', 'email_address', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_type', 'hash_md5', 'hash_sha256', 'mime', 'operation', 'src_ip', 'time', 'url', 'user'] |
| edit_regex_field | dest_host |  | ['"destinationName":"({device_name}({dest_host}[\w\-\.]+))"'] |
| edit_regex_field | operation |  | ['"eventType":"({access_type}({operation}[^"]+))"'] |
| added_regex_field | access_type |  | ['"eventType":"({access_type}({operation}[^"]+))"'] |
| added_regex_field | device_name |  | ['"destinationName":"({device_name}({dest_host}[\w\-\.]+))"'] |
| removed_attribute | DupFields |  | N/A |