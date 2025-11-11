# Code Changes for microsoft-windows-kv-dhcp-session-success-dns (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'dest_ip', 'dest_mac', 'host', 'time', 'user'] |
| added_regex_field | user |  | [',(DNS.*)?(更新|要求|成功|更新成功)([^,]+)?,([^,]+,)({user}[\w\.\-]{1,40}\$?)'] |
| removed_attribute | DupFields |  | N/A |