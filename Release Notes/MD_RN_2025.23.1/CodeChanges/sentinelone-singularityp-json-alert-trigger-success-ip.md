# Code Changes for sentinelone-singularityp-json-alert-trigger-success-ip (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'dest_ip', 'dest_port', 'domain', 'event_name', 'hash_md5', 'hash_sha1', 'hash_sha256', 'host', 'host_type', 'os', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'src_ip', 'src_port', 'time', 'user', 'user_agent'] |
| added_regex_field | dest_host |  | ['"endpoint\.name":"({dest_host}[^"]+)'] |
| removed_attribute | DupFields |  | N/A |