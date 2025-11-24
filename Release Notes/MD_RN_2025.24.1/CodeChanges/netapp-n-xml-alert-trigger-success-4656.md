# Code Changes for netapp-n-xml-alert-trigger-success-4656 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'alert_name', 'alert_type', 'domain', 'event_code', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'object_class', 'object_id', 'object_server', 'process_dir', 'process_name', 'process_path', 'result', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | object_class |  | ['<Data Name\\*="*ObjectType"*>({alert_type}({object_class}.+?))<\/Data>'] |
| added_regex_field | alert_type |  | ['<Data Name\\*="*ObjectType"*>({alert_type}({object_class}.+?))<\/Data>'] |
| removed_attribute | DupFields |  | N/A |