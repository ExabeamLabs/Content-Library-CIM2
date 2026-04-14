# Code Changes for microsoft-evapplocker-xml-alert-trigger-success-policyname (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'alert_severity', 'alert_type', 'channel', 'domain', 'event_code', 'hash_md5', 'hash_sha1', 'hash_sha256', 'host', 'malware_url', 'process_dir', 'process_name', 'process_path', 'run_level', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<\/Channel>'] |