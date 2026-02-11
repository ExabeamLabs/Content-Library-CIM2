# Code Changes for microsoft-o365-json-email-send-fail-publish (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['attachment_count', 'bytes', 'category', 'compauth_result', 'connectors', 'dest_email_address', 'dest_email_domain', 'direction', 'dkim_result', 'dmarc_result', 'email_address', 'email_domain', 'email_subject', 'file_verdict', 'message_id', 'operation', 'result', 'spf_result', 'src_ip', 'src_port', 'time', 'url_count'] |
| added_regex_field | bytes |  | ['"EmailSize":({bytes}\d+)'] |