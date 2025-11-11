# Code Changes for cef-juniper-vpn-events (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'dest_port', 'email_address', 'host', 'result', 'src_host', 'src_ip', 'src_port', 'src_translated_ip', 'time', 'user'] |
| added_regex_field | account |  | ['\Wsuser=({account}[\w\.\-\!\#\^\~]{1,40}\$?)'] |
| removed_attribute | DupFields |  | N/A |