# Code Changes for microsoft-evsystem-xml-dcom-activate-fail-10016 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'cls_id', 'domain', 'event_code', 'host', 'login_id', 'opcode', 'process_id', 'result_code', 'run_level', 'src_domain', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |