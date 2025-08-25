# Code Changes for osirium-o-str-app-login-success-logged (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| removed_parser | N/A | {"Name": "osirium-o-str-app-login-success-logged", "Vendor": "Osirium", "Product": "Osirium", "TimeFormat": "yyyy-MM-dd HH:mm:ss", "Conditions": [":User u'", " logged "], "Fields": [":User u\'({user}[\w\.\-\!\#\^\~]{1,40}\$?)'", "address\s*\'({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\'\s*logged", "({app}osirium)"], "ParserVersion": "v1.0.0"} | N/A |