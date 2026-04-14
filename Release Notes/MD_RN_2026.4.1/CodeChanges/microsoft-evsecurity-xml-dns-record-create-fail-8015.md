# Code Changes for microsoft-evsecurity-xml-dns-record-create-fail-8015 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'cls_id', 'domain', 'event_code', 'failure_code', 'failure_reason', 'host', 'login_id', 'process_id', 'result_code', 'run_level', 'src_domain', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |