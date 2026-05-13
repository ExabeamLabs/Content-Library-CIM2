# Code Changes for logrhythm-o365-app-activity (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'channel', 'domain', 'email_address', 'event_name', 'file_ext', 'file_name', 'file_type', 'object', 'operation', 'result', 'src_ip', 'src_port', 'time', 'user', 'user_agent'] |
| added_regex_field | channel |  | ['"Channel"+:"+({channel}[^"]+)"', '<Channel>({channel}[^<]+)<'] |