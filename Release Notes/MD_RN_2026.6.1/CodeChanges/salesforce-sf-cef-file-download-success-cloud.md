# Code Changes for salesforce-sf-cef-file-download-success-cloud (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['\Wsuser=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\\s@;=]+)\\+)?(system|anonymous|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+(\w+=|$)'] |
| edit_regex_field | email_address |  | ['\Wsuser=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\\s@;=]+)\\+)?(system|anonymous|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+(\w+=|$)'] |
| edit_regex_field | email_domain |  | ['\Wsuser=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\\s@;=]+)\\+)?(system|anonymous|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+(\w+=|$)'] |
| edit_regex_field | user |  | ['\Wsuser=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\\s@;=]+)\\+)?(system|anonymous|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+(\w+=|$)'] |