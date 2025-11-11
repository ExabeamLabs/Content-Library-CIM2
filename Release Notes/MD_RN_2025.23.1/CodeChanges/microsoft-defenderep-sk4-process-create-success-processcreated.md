# Code Changes for microsoft-defenderep-sk4-process-create-success-processcreated (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['category', 'dest_host', 'dest_ip', 'dest_port', 'device_id', 'direction', 'domain', 'event_hub_name', 'event_hub_namespace', 'event_name', 'hash_md5', 'hash_sha1', 'hash_sha256', 'host', 'operation', 'parent_process_dir', 'parent_process_name', 'parent_process_path', 'process_command_line', 'process_dir', 'process_id', 'process_integrity', 'process_name', 'process_path', 'product_name', 'protocol', 'result', 'src_ip', 'src_port', 'time', 'url', 'user', 'user_sid', 'web_domain'] |
| edit_regex_field | category |  | ['"category\\?"+:\s*\\?"+({event_name}({category}[^"]+?))\\?"'] |
| edit_regex_field | event_hub_name |  | ['\[Namespace:\s*({host}({event_hub_namespace}\S+)) ; EventHub name:\s*({event_hub_name}[\w-]+)'] |
| edit_regex_field | event_hub_namespace |  | ['\[Namespace:\s*({host}({event_hub_namespace}\S+)) ; EventHub name:\s*({event_hub_name}[\w-]+)'] |
| added_regex_field | event_name |  | ['"category\\?"+:\s*\\?"+({event_name}({category}[^"]+?))\\?"'] |
| added_regex_field | host |  | ['\[Namespace:\s*({host}({event_hub_namespace}\S+)) ; EventHub name:\s*({event_hub_name}[\w-]+)'] |
| removed_attribute | DupFields |  | N/A |