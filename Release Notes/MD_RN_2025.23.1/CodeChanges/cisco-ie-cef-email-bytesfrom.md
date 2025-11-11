# Code Changes for cisco-ie-cef-email-bytesfrom (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'bytes', 'dest_email_address', 'dest_email_domain', 'email_address', 'email_domain', 'host', 'message_id', 'src_ip', 'time'] |
| added_regex_field | message_id |  | ['MID ({message_id}\d+)'] |
| removed_attribute | DupFields |  | N/A |