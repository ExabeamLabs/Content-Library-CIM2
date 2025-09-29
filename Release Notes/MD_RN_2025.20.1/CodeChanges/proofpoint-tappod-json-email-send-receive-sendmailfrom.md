# Code Changes for proofpoint-tappod-json-email-send-receive-sendmailfrom (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['"to":\["<\\'?({dest_email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@([^\]\s"\\,\|>]+\.[^\]\s"\\,\|>]+)(?<!local))\s*>', 'exa_regex="to":\["<\\'?({dest_email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@([^\]\s"\\,\|>]+\.[^\]\s"\\,\|>]+)(?<!local))\s*>'] |