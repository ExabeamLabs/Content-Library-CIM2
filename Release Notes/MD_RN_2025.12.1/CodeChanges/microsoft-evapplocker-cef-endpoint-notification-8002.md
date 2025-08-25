# Code Changes for microsoft-evapplocker-cef-endpoint-notification-8002 (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| changed_parsed_fields | N/A | ['domain', 'event_code', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'hash_md5', 'host', 'login_id', 'process_name', 'time', 'user', 'user_sid'] | ['domain', 'event_code', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'hash_md5', 'hash_sha1', 'hash_sha256', 'host', 'login_id', 'process_name', 'time', 'user', 'user_sid'] |
| edit_regex_field | hash_md5 | ['"FileHash":"({hash_md5}[^"]+)'] | ['"FileHash":"(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))"'] |
| added_regex_field | hash_sha1 | [] | ['"FileHash":"(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))"'] |
| added_regex_field | hash_sha256 | [] | ['"FileHash":"(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))"'] |