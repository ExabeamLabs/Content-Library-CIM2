# Code Changes for eset-es-cef-alert-trigger-success-eventtype (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'alert_severity', 'alert_type', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'host', 'malware_url', 'process_name', 'process_path', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | host |  | ['({dest_host}({host}[^\s]+))\sERAServer\s'] |
| added_regex_field | dest_host |  | ['({dest_host}({host}[^\s]+))\sERAServer\s'] |
| removed_attribute | DupFields |  | N/A |