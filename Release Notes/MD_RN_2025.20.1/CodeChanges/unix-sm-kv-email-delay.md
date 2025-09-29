# Code Changes for unix-sm-kv-email-delay (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'bytes', 'dest_email_address', 'dest_host', 'dest_ip', 'host', 'host_ip', 'process_id', 'process_name', 'result'] |
| added_regex_field | process_id |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |
| added_regex_field | process_name |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |