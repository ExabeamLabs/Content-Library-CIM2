# Code Changes for infoblox-bddi-str-configuration-modify-success-named (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'host', 'host_record', 'operation', 'process_id', 'process_name', 'zone'] |
| added_regex_field | process_id |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*', '\s+({process_name}\S+)\[({process_id}\d+)\]\:\s+'] |
| added_regex_field | process_name |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*', '\s+({process_name}\S+)\[({process_id}\d+)\]\:\s+'] |