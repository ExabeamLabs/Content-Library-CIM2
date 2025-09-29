# Code Changes for unix-sm-kv-email-send (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'bytes', 'dest_host', 'dest_ip', 'dest_port', 'email_address', 'email_domain', 'host', 'host_ip', 'num_recipients', 'process_id', 'process_name', 'protocol', 'return_path', 'time', 'user'] |
| added_regex_field | process_id |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |
| added_regex_field | process_name |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |