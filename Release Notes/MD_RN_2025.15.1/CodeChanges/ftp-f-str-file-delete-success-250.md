# Code Changes for ftp-f-str-file-delete-success-250 (Parser)

| Code Change | Field Name | 2025.14.1 | 2025.15.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | src_ip | ['({src_ip}\S+)\s+(\S+\s+){2}\[\d+\]'] | ['({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s+(\S+\s+){2}\[\d+\]'] |