# Code Changes for appsense-am-leef-alert-trigger-success-warning (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A | ['alert_name', 'alert_severity', 'dest_host', 'dest_user_sid', 'domain', 'hash_md5', 'process_dir', 'process_name', 'process_path', 'process_vendor', 'time', 'user'] | ['alert_name', 'alert_severity', 'dest_host', 'dest_user_sid', 'domain', 'hash_md5', 'hash_sha1', 'hash_sha256', 'process_dir', 'process_name', 'process_path', 'process_vendor', 'time', 'user'] |
| edit_regex_field | hash_md5 | ['Hash:({hash_md5}[^\s\]]+)'] | ['Hash:(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))'] |
| added_regex_field | hash_sha1 | [] | ['Hash:(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))'] |
| added_regex_field | hash_sha256 | [] | ['Hash:(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))'] |