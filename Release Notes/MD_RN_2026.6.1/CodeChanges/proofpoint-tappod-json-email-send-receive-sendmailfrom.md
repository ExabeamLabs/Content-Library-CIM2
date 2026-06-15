# Code Changes for proofpoint-tappod-json-email-send-receive-sendmailfrom (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['"to":\["<\\'?({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@([^\]\s"\\,\|>]+\.[^\]\s"\\,\|>]+)(?<!local))\s*>', 'exa_regex="to":\["<\\'?({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@([^\]\s"\\,\|>]+\.[^\]\s"\\,\|>]+)(?<!local))\s*>'] |
| edit_regex_field | email_address |  | ['"from"+:\s*\[?"+([^<,]+?<|<)?(\\u\d+)?({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|\>]+\.[^\]\s"\\,;\|\>]+))\s*>?', 'exa_json_path=$.sm.from,exa_regex=([^<,]+?<|<)?(\\u\d+)?({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|\>]+\.[^\]\s"\\,;\|\>]+))\s*>?'] |
| edit_regex_field | email_domain |  | ['"from"+:\s*\[?"+([^<,]+?<|<)?(\\u\d+)?({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|\>]+\.[^\]\s"\\,;\|\>]+))\s*>?', 'exa_json_path=$.sm.from,exa_regex=([^<,]+?<|<)?(\\u\d+)?({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|\>]+\.[^\]\s"\\,;\|\>]+))\s*>?'] |