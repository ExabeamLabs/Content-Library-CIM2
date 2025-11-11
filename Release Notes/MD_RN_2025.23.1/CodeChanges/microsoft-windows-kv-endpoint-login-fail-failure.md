# Code Changes for microsoft-windows-kv-endpoint-login-fail-failure (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'login_type', 'result_code', 'src_ip', 'src_port', 'src_user', 'time', 'user'] |
| edit_regex_field | event_code |  | ['\|McAfee\|[^|]+?\|[^|]+?\|43-21100({result_code}({event_code}\d+))(0|1)\|'] |
| edit_regex_field | host |  | ['deviceTranslatedAddress=({dest_host}({host}[a-fA-F:\d.]+))'] |
| added_regex_field | dest_host |  | ['deviceTranslatedAddress=({dest_host}({host}[a-fA-F:\d.]+))'] |
| added_regex_field | result_code |  | ['\|McAfee\|[^|]+?\|[^|]+?\|43-21100({result_code}({event_code}\d+))(0|1)\|'] |
| removed_attribute | DupFields |  | N/A |