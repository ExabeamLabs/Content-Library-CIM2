# Code Changes for microsoft-o365-cef-email-send-sendas (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| changed_parsed_fields | N/A | ['account_name', 'additional_info', 'alert_name', 'app', 'bytes', 'email_address', 'email_attachment', 'email_attachments', 'email_domain', 'email_subject', 'first_name', 'full_name', 'host', 'last_name', 'result', 'src_ip', 'src_port', 'time', 'user_id', 'user_type'] | ['account_name', 'additional_info', 'alert_name', 'app', 'bytes', 'email_address', 'email_attachment', 'email_attachments', 'email_domain', 'email_subject', 'first_name', 'full_name', 'host', 'last_name', 'result', 'src_ip', 'src_port', 'time', 'user_agent', 'user_id', 'user_type'] |
| added_regex_field | user_agent | [] | ['"ActorInfoString\\*"+:[\s\\]*"({user_agent}[^"\\]+)'] |