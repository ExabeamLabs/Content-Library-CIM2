# Code Changes for proofpoint-tap-sk4-email-routedirection (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['bytes', 'dest_email_address', 'dest_email_domain', 'direction', 'email_address', 'email_attachment', 'email_attachments', 'email_domain', 'email_recipients', 'email_subject', 'is_consolidated', 'result', 'rule', 'time'] |
| edit_regex_field | email_attachment |  | ['"detectedName":\s*"({email_attachments}({email_attachment}(?!text)[^"]+))'] |
| added_regex_field | email_attachments |  | ['"detectedName":\s*"({email_attachments}({email_attachment}(?!text)[^"]+))'] |
| removed_attribute | DupFields |  | N/A |