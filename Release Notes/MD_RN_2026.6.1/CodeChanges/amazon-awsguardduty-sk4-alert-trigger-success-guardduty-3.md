# Code Changes for amazon-awsguardduty-sk4-alert-trigger-success-guardduty-3 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | aws_account |  | ['"userName\\?":\\?"(({aws_email_address}({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))|({aws_account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| edit_regex_field | aws_email_address |  | ['"userName\\?":\\?"(({aws_email_address}({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))|({aws_account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| edit_regex_field | email_address |  | ['"userName\\?":\\?"(({aws_email_address}({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))|({aws_account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| edit_regex_field | email_domain |  | ['"userName\\?":\\?"(({aws_email_address}({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))|({aws_account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| edit_regex_field | user |  | ['"userName\\?":\\?"(({aws_email_address}({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))|({aws_account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |