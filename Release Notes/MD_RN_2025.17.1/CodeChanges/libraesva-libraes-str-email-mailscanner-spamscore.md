# Code Changes for libraesva-libraes-str-email-mailscanner-spamscore (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| added_parser | N/A |  | {"Name": "libraesva-libraes-str-email-mailscanner-spamscore", "Vendor": "Libraesva", "Product": "Libraesva Email Security", "TimeFormat": ["MMM dd HH:mm:ss", "MMM d HH:mm:ss"], "Conditions": [" MailScanner[", "]: ", " SpamAssassin "], "Fields": ["({time}\w{3}\s+\d{1,2}\s+\d\d:\d\d:\d\d)\s+({host}[^\s]+)\s", "\W(M|m)essage ({message_id}\S+)\s", "\sfrom ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))? [\(]", "\Wscore=({spam_score}[^,)]+)"], "ParserVersion": "v1.0.0"} |