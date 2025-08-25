# Code Changes for box-ccm-json-file-download-success-manageddevice (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'bytes', 'dest_host', 'dest_ip', 'device_id', 'email_address', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_type', 'hash_md5', 'hash_sha256', 'mime', 'operation', 'src_ip', 'time', 'url', 'user'] |
| edit_regex_field | email_address |  | ['"deviceUserName":"({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"', '"operatingSystemUser":"(({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| removed_regex_field | file_path |  | [] |
| edit_regex_field | user |  | ['"operatingSystemUser":"(({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| added_regex_field | file_dir |  | ['"filePath":"({file_dir}[^"]+)"'] |