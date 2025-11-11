# Code Changes for sentinelone-singularityp-json-registry-create-success-valuecreate (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_name', 'alert_type', 'dest_domain', 'dest_host', 'dest_user', 'domain', 'event_name', 'hash_md5', 'hash_sha1', 'hash_sha256', 'host', 'host_type', 'object', 'operation', 'os', 'process_dir', 'process_id', 'process_name', 'process_path', 'registry_key', 'registry_path', 'registry_value', 'time', 'user', 'user_agent'] |
| edit_regex_field | alert_name |  | ['"event\.type":"({event_name}({alert_name}[^"]+))'] |
| edit_regex_field | host |  | ['"endpoint\.name":"({dest_host}({host}[^"]+))'] |
| added_regex_field | dest_host |  | ['"endpoint\.name":"({dest_host}({host}[^"]+))'] |
| added_regex_field | event_name |  | ['"event\.type":"({event_name}({alert_name}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |