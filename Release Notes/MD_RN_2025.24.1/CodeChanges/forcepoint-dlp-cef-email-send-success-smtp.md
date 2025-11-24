# Code Changes for forcepoint-dlp-cef-email-send-success-smtp (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_name', 'alert_severity', 'alert_type', 'attachment', 'bytes', 'bytes_unit', 'dest_email_address', 'dest_email_domain', 'dest_host', 'dest_ip', 'domain', 'email_address', 'email_attachment', 'email_attachments', 'email_subject', 'file_ext', 'file_name', 'first_name', 'full_name', 'host', 'last_name', 'result', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | email_attachment |  | ['\Wfname=\s*(N\/A|-|({attachment}({email_attachments}({email_attachment}[^=;]+)[^=]*)))\s([\w\.]+=|$)', '\Wfname=\s*({email_attachment}[^;]+?)(;.*?)?\s*([\w\.]+=|$)'] |
| edit_regex_field | email_attachments |  | ['\Wfname=\s*(N\/A|-|({attachment}({email_attachments}({email_attachment}[^=;]+)[^=]*)))\s([\w\.]+=|$)'] |
| added_regex_field | attachment |  | ['\Wfname=\s*(N\/A|-|({attachment}({email_attachments}({email_attachment}[^=;]+)[^=]*)))\s([\w\.]+=|$)'] |
| removed_attribute | DupFields |  | N/A |