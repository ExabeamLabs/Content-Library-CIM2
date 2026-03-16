# Code Changes for sentinelone-singularityp-json-driver-load-success-driverload (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_domain', 'dest_host', 'dest_user', 'dest_user_full_name', 'domain', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'file_signed', 'hash_md5', 'hash_sha1', 'hash_sha256', 'host', 'os', 'process_dir', 'process_id', 'process_name', 'process_path', 'time', 'user', 'user_agent'] |
| added_regex_field | file_signed |  | ['"src.process.signedStatus":\s*\\?"+({file_signed}[^"\\]+)"'] |