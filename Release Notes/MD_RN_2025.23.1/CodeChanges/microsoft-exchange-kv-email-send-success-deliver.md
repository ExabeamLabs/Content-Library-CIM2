# Code Changes for microsoft-exchange-kv-email-send-success-deliver (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_id', 'alert_name', 'alert_type', 'bytes', 'dest_email_address', 'dest_email_domain', 'dest_host', 'dest_ip', 'dest_port', 'email_address', 'email_recipients', 'email_subject', 'num_recipients', 'orig_user', 'return_path', 'src_host', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | email_address |  | ['\ssender-address=(?:|({orig_user}({email_address}[^@]+@[^\s;]+)))\s*[\w\-]+='] |
| added_regex_field | alert_type |  | ['\tsource=(?:|({alert_type}.+?))\t[\w\-]+='] |
| added_regex_field | orig_user |  | ['\ssender-address=(?:|({orig_user}({email_address}[^@]+@[^\s;]+)))\s*[\w\-]+='] |
| removed_attribute | DupFields |  | N/A |