# Code Changes for microsoft-o365-json-email-send-fail-advancedhunting (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['attachment_size', 'category', 'dest_email_address', 'dest_email_domain', 'email_address', 'email_attachment', 'file_ext', 'file_hash', 'file_name', 'file_type', 'message_id', 'time'] |
| removed_regex_field | bytes |  | [] |
| added_regex_field | attachment_size |  | ['"FileSize":({attachment_size}\d+)'] |