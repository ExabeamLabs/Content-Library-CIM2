# Code Changes for hp-arubaos-str-ssh-close-success-sshclose (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| added_parser | N/A |  | {"Name": "hp-arubaos-str-ssh-close-success-sshclose", "ParserVersion": "v1.0.0", "Vendor": "HP", "Product": "ArubaOS", "TimeFormat": "yyyy-MM-dd'T'HH:mm:ss", "Conditions": [" %SSH", "-SSH_CLOSE:", "SSH Session "], "Fields": ["\s({host}[\w\-\.]+):\s\d+-\d+-\d+", "SSH Session from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?", "for user '({user}[\w\.\-]{1,40}\$?)'", "({time}\d+-\d+-\d+T\d+:\d+:\d+)"]} |