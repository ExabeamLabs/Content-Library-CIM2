# Code Changes for proofpoint-tappod-json-email-receive-fail-emailreceived (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['bytes', 'dest_email_address', 'dest_email_domain', 'direction', 'email_address', 'email_attachment', 'email_attachments', 'email_domain', 'email_recipients', 'email_subject', 'file_ext', 'full_name', 'host', 'message_id', 'result', 'return_path', 'rule', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | email_attachment |  | ['exa_regex=msgParts":[^\n]*?"detectedName":"({email_attachments}({email_attachment}[^"]+))"', 'msgParts":[^\n]*?"detectedName":"({email_attachments}({email_attachment}[^"]+))"'] |
| added_regex_field | email_attachments |  | ['exa_regex=msgParts":[^\n]*?"detectedName":"({email_attachments}({email_attachment}[^"]+))"', 'msgParts":[^\n]*?"detectedName":"({email_attachments}({email_attachment}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |