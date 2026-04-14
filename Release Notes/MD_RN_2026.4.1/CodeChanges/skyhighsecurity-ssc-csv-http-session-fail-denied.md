# Code Changes for skyhighsecurity-ssc-csv-http-session-fail-denied (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'app', 'categories', 'country_code', 'dest_ip', 'dest_port', 'failure_reason', 'log_source', 'method', 'mime', 'protocol', 'result_code', 'src_host', 'src_ip', 'src_translated_ip', 'time', 'url', 'user', 'user_agent'] |
| added_regex_field | user_agent |  | ['Logging-Client.*?DENIED","(([^"]*"),"){15}({user_agent}[^"]+)'] |