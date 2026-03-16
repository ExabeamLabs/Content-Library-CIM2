# Code Changes for google-workspace-cef-email-receive (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'app', 'attachment_count', 'bytes', 'dest_email_address', 'dest_email_domain', 'email_address', 'email_attachment', 'email_subject', 'message_id', 'result', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | email_address |  | ['"source":\{"address":"({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)', 'exa_json_path=$.message_info.source.address,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)'] |
| removed_regex_field | email_domain |  | [] |