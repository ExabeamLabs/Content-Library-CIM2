# Code Changes for nextdlp-r-json-configuration-modify-success-reveal (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'app', 'bytes', 'bytes_unit', 'dest_ip', 'dest_port', 'domain', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'first_name', 'full_name', 'host', 'last_name', 'process_dir', 'process_name', 'process_path', 'src_host', 'src_ip', 'src_port', 'tag', 'time', 'url', 'user'] |
| edit_regex_field | host |  | ['"agent_hostname":\s*"({src_host}({host}[\w\-\.]+))"'] |
| added_regex_field | src_host |  | ['"agent_hostname":\s*"({src_host}({host}[\w\-\.]+))"'] |
| removed_attribute | DupFields |  | N/A |