# Code Changes for microsoft-evapp-xml-ssh-traffic-success-sshd_accepted (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'dest_host', 'event_code', 'event_id', 'host', 'process_id', 'protocol', 'result', 'run_level', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<\/Channel>'] |