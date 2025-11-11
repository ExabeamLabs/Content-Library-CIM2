# Code Changes for microsoft-exchange-kv-email-send-originating-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'alert_name', 'alert_type', 'bytes', 'dest_email_address', 'dest_email_domain', 'dest_host', 'dest_ip', 'dest_port', 'direction', 'email_address', 'email_domain', 'email_recipients', 'email_subject', 'num_recipients', 'orig_user', 'result', 'src_host', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | email_address |  | ['sender-address=({orig_user}({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))'] |
| edit_regex_field | email_domain |  | ['sender-address=({orig_user}({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))'] |
| added_regex_field | alert_type |  | ['\tsource=(?:|({alert_type}.+?))\t[\w\-]+='] |
| added_regex_field | orig_user |  | ['sender-address=({orig_user}({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))'] |
| removed_attribute | DupFields |  | N/A |