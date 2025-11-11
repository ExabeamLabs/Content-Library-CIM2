# Code Changes for microsoft-o365-json-email-send-fail-advancedhunting (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['bytes', 'category', 'dest_email_address', 'dest_email_domain', 'email_address', 'email_attachment', 'file_ext', 'file_hash', 'file_name', 'file_type', 'message_id', 'time'] |
| edit_regex_field | file_ext |  | ['"FileName":\s*"({email_attachment}({file_name}[^"\.]+?(\.({file_ext}[^"]+?)))?)"'] |
| edit_regex_field | file_name |  | ['"FileName":\s*"({email_attachment}({file_name}[^"\.]+?(\.({file_ext}[^"]+?)))?)"'] |
| added_regex_field | email_attachment |  | ['"FileName":\s*"({email_attachment}({file_name}[^"\.]+?(\.({file_ext}[^"]+?)))?)"'] |
| removed_attribute | DupFields |  | N/A |