# Code Changes for microsoft-rras-kv-vpn-logout-success-coid (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'session_id', 'src_translated_ip'] |
| added_regex_field | channel |  | ['"Channel"+:"+({channel}[^"]+)"'] |