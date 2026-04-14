# Code Changes for exa-events-ns (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'dest_ip', 'dest_port', 'security_criticality', 'src_host', 'src_ip', 'src_port', 'trigger_time', 'user'] |
| added_regex_field | trigger_time |  | ['exa_json_path=$.trigger_time,exa_regex=({trigger_time}\d{10,13})'] |
| added_attribute | trigger_timeFormat |  | ['epoch_sec', 'epoch'] |