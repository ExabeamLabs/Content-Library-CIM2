# Code Changes for q-exchange-dlp-email-out (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['\trecipient-address="?(?:|({email_recipients}({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)).*?))"?\t[\w\-]+='] |
| edit_regex_field | dest_email_domain |  | ['\trecipient-address="?(?:|({email_recipients}({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)).*?))"?\t[\w\-]+='] |
| edit_regex_field | email_address |  | ['\tsender-address=(?:|({orig_user}({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))))\t[\w\-]+='] |
| edit_regex_field | email_domain |  | ['\tsender-address=(?:|({orig_user}({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))))\t[\w\-]+='] |
| edit_regex_field | email_recipients |  | ['\trecipient-address="?(?:|({email_recipients}({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)).*?))"?\t[\w\-]+='] |
| edit_regex_field | orig_user |  | ['\tsender-address=(?:|({orig_user}({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))))\t[\w\-]+='] |