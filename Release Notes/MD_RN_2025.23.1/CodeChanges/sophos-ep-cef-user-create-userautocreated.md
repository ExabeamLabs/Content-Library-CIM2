# Code Changes for sophos-ep-cef-user-create-userautocreated (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'app', 'domain', 'full_name', 'host', 'malware_url', 'process_name', 'process_path', 'src_host', 'src_ip', 'src_port', 'target', 'time', 'user'] |
| added_regex_field | src_host |  | ['"location":"({src_host}[\w\-.]+)"'] |
| removed_attribute | DupFields |  | N/A |