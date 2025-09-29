# Code Changes for proofpoint-tappod-json-email-send-receive-sendmailto (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['"to"+:\s*\["+(\\u\d+)?<(([^<@\]]+<|<|\\"+|\\')?({dest_email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@([^\]\s"\\,\|>]+\.[^\]\s"\\,\|>]+)(?<!local)))\s*>', 'exa_json_path=$.sm.to[1:],exa_regex=(\\u\d+)?<(([^<@\]]+<|<|\\"+|\\')?({dest_email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@([^\]\s"\\,\|>]+\.[^\]\s"\\,\|>]+)(?<!local)))\s*>', 'exa_regex="to":\s*\["?<\\'?({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|\>]+))'] |
| edit_regex_field | dest_email_domain |  | ['exa_regex="to":\s*\["?<\\'?({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|\>]+))'] |