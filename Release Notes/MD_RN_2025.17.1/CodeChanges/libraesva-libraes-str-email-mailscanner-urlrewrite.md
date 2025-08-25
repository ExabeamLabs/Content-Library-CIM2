# Code Changes for libraesva-libraes-str-email-mailscanner-urlrewrite (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| added_parser | N/A |  | {"Name": "libraesva-libraes-str-email-mailscanner-urlrewrite", "Vendor": "Libraesva", "Product": "Libraesva Email Security", "TimeFormat": ["MMM dd HH:mm:ss", "MMM d HH:mm:ss"], "Conditions": [" MailScanner[", " of message ", " URLSand "], "Fields": ["({time}\w{3}\s+\d{1,2}\s+\d\d:\d\d:\d\d)\s+({host}[^\s]+)\s", ":\sURLSand rewrite URL\s({url}[^\s]+)\sin\s({additional_info}\S+)\s", "\Wof message ({message_id}\S+)"], "ParserVersion": "v1.0.0"} |