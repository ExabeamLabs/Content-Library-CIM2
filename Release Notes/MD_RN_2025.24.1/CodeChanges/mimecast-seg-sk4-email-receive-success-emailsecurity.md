# Code Changes for mimecast-seg-sk4-email-receive-success-emailsecurity (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'category', 'dest_email_address', 'dest_email_domain', 'direction', 'email_address', 'email_domain', 'email_subject', 'message_id', 'operation', 'result_reason', 'src_ip', 'src_port', 'time', 'url'] |
| edit_regex_field | action |  | ['"action":"({operation}({action}[^"]+))"'] |
| added_regex_field | operation |  | ['"action":"({operation}({action}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |