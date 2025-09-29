# Code Changes for unix-unix-str-dns-record-create-success-registeringnewaddress (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'event_name', 'process_id', 'process_name', 'src_ip'] |
| added_regex_field | process_id |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*', '\s+({process_name}\S+)\[({process_id}\d+)\]\:\s+'] |
| added_regex_field | process_name |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*', '\s+({process_name}\S+)\[({process_id}\d+)\]\:\s+'] |