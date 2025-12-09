# Code Changes for microsoft-evsecurity-kv-share-access-success-5145 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'access_mask', 'access_reason', 'dest_host', 'domain', 'event_code', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'file_type', 'host', 'login_id', 'result', 'share_name', 'share_path', 'src_ip', 'src_port', 'user', 'user_sid'] |
| added_regex_field | result |  | ['Security:\s*({result}[^\(]+)\(\d+\):'] |
| edit_attribute | activity_type |  | ['share-access:fail', 'share-access:success'] |
| edit_attribute | legacy_activity_type |  | ['share-access', 'share-access-denied'] |