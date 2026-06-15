# Code Changes for amazon-awscloudtrail-json-app-activity-success-getrolecredentials (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | aws_account |  | ['exa_json_path=$.userIdentity.userName,exa_regex=(({aws_email_address}({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({aws_account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| edit_regex_field | aws_email_address |  | ['exa_json_path=$.userIdentity.userName,exa_regex=(({aws_email_address}({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({aws_account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| edit_regex_field | email_address |  | ['exa_json_path=$.userIdentity.userName,exa_regex=(({aws_email_address}({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({aws_account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| edit_regex_field | user |  | ['exa_json_path=$.userIdentity.userName,exa_regex=(({aws_email_address}({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({aws_account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |