# Code Changes for unix-unix-str-endpoint-login-fail-sshdauthfailed (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_ip', 'dest_port', 'event_code', 'failure_reason', 'host', 'process_id', 'process_name', 'protocol', 'src_ip', 'src_port', 'user'] |
| added_regex_field | process_id |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |
| added_regex_field | process_name |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |