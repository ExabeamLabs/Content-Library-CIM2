# Code Changes for microsoft-exchange-json-email-receive-incoming (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_id', 'alert_name', 'alert_type', 'bytes', 'dest_email_address', 'dest_email_domain', 'dest_host', 'dest_ip', 'dest_port', 'email_address', 'email_domain', 'email_recipients', 'email_subject', 'num_recipients', 'orig_user', 'return_path', 'src_host', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | dest_email_address |  | ['recipient_address":"({orig_user}({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))'] |
| edit_regex_field | dest_email_domain |  | ['recipient_address":"({orig_user}({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))'] |
| added_regex_field | alert_type |  | ['exchange_source":"(?:|({alert_type}[^"]+))",'] |
| added_regex_field | orig_user |  | ['recipient_address":"({orig_user}({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))'] |
| removed_attribute | DupFields |  | N/A |