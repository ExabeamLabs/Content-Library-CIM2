# Code Changes for microsoft-evsystem-xml-service-state-modify-7036-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['event_code', 'event_name', 'host', 'process_id', 'run_level', 'service_name', 'service_state', 'src_host', 'time'] |
| edit_regex_field | service_name |  | ['<Data Name\\*=(\'|")param1(\'|")>({service_name}[^<]+)<', 'The ({service_name}[^\.="]+) service entered the ({service_state}[^\.="]+) state'] |
| added_regex_field | service_state |  | ['The ({service_name}[^\.="]+) service entered the ({service_state}[^\.="]+) state'] |