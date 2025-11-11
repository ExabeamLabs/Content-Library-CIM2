# Code Changes for q-exchange-dlp-email-out (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_id', 'alert_name', 'alert_type', 'bytes', 'dest_email_address', 'dest_email_domain', 'dest_host', 'dest_ip', 'dest_port', 'eamil_subject', 'email_address', 'email_domain', 'email_recipients', 'num_recipients', 'orig_user', 'return_path', 'src_host', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | email_address |  | ['\tsender-address=(?:|({orig_user}({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))))\t[\w\-]+='] |
| edit_regex_field | email_domain |  | ['\tsender-address=(?:|({orig_user}({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))))\t[\w\-]+='] |
| added_regex_field | alert_type |  | ['\tsource=(?:|({alert_type}.+?))\t[\w\-]+='] |
| added_regex_field | orig_user |  | ['\tsender-address=(?:|({orig_user}({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))))\t[\w\-]+='] |
| removed_attribute | DupFields |  | N/A |