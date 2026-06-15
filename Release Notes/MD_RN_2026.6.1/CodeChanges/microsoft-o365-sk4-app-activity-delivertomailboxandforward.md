# Code Changes for microsoft-o365-sk4-app-activity-delivertomailboxandforward (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'correlation_id', 'dest_email_address', 'dest_email_domain', 'email_address', 'email_domain', 'email_recipients', 'mailbox_name', 'object', 'operation', 'result', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | dest_email_address |  | ['Forward.+?Value":"(smtp:)?({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"'] |
| edit_regex_field | dest_email_domain |  | ['"Value":"(smtp:)?[^@"]+@({dest_email_domain}[^"]+?)"', 'Forward.+?Value":"(smtp:)?({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"'] |
| added_regex_field | email_recipients |  | ['"Name":"Forward[^\}]+?Value":"(smtp:)?({email_recipients}[^"]+@[^"]+)'] |
| added_regex_field | mailbox_name |  | ['"ObjectId\\*"+:"?[\s\\]*"+(Unknown|Not Available|({object}({mailbox_name}[^"]+)))'] |
| added_regex_field | object |  | ['"ObjectId\\*"+:"?[\s\\]*"+(Unknown|Not Available|({object}({mailbox_name}[^"]+)))'] |