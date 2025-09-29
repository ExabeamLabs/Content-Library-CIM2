# Code Changes for unix-unix-str-alert-trigger-sshdbreakinattempt (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'host', 'process_id', 'process_name', 'src_host', 'src_ip', 'src_port'] |
| edit_regex_field | process_name |  | ['({host}[\w.\-]+) ({process_name}sshd)\[', '\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |
| added_regex_field | process_id |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |